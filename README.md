# projeto-LH-Pets
namespace Projeto_Web_Lh_Pets_Alunos_1;

public class Program
{
    public static void Main(string[] args)
    {
        var builder = WebApplication.CreateBuilder(args);
        var app = builder.Build();

        app.MapGet("/", () => "Projeto Web LH Pets Versão 1");

app.UseStatiscFiles ();
app.MapGet("/index", (HttpContext contexto)=> {contexto.Response.Redirect("index.html", false)});

        app.Run();
    }
}
