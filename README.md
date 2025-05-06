[Link na dennik](https://docs.google.com/document/d/1WGTlvpBF4o0pcz3C6o_jY1h78R7Gm7IU/edit?fbclid=IwZXh0bgNhZW0CMTEAAR2OxAc1jh-fdmE2KE5hjyNs7KKp72I0yIn5ktrYmgxSTyrpAXPlWZE87-E_aem_J-4SCwqBWAFCQ_ulnsVWtA#heading=h.dchu1jahv1pi)

Pridajte si do `.git/config` tento riadok, aby ste necommitovali outputy -> omnoho lahsie sa potom merguje. Mozete to ignorovat, ak nemate subor do ktoreho budu pisat viaceri.
```
[filter "strip-notebook-output"]
	clean = "jupyter nbconvert --ClearOutputPreprocessor.enabled=True --ClearMetadataPreprocessor.enabled=True --to=notebook --stdin --stdout --log-level=ERROR"
```