<%*
const title = await tp.system.prompt("Titolo del film");
if (title) await tp.file.rename(title);
const director = await tp.system.prompt("Regista");
const year = await tp.system.prompt("Anno");
const status = await tp.system.suggester(["Da vedere", "Visto"], ["to-watch", "watched"]);
-%>
---
director: <% director ? `"[[${director}]]"` : "" %>
year: <% year %>
genre: []
status: <% status ?? "to-watch" %>
available_on:
watched_on: <% status === "watched" ? tp.date.now("YYYY-MM-DD") : "" %>
owned: false
worth_owning: false
---

# Trama


***

# I miei pensieri e recensione


***

# Citazioni preferite
> (Inserisci qui le frasi che ti hanno colpito di più)
