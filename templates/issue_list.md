| newChapter2| Issue Title  | Issue Status | Severity |
| ------------- | ------------- | ------------- | ------------- |
<% issues_ordered_with_links.each_with_index do |issue,index| %> | 3.<%= index+1 %> | [<%= issue["title"] %>](<%= issue["link"] %>) | <% if !standalone %> <img height="30px" src="static-content/<%= issue["state"].to_s.downcase %>.png"/> <% else %> <%= issue["state"].to_s.downcase.capitalize %>  <% end %>| <% if !standalone %>  <img height="30px" src="static-content/<%=issue["severity"].to_s.downcase %>.png"/>  <% else %> <%= issue["severity"].to_s.downcase.capitalize %>  <% end %>| 
<% end %>
