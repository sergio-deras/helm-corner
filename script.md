```
{{ -if .Values.img.tag }}
  bla:
    bla: {{ .Values.img.tag }}


{{ .Values.firstOne | quote }}


{{ .Values.firstOne | <function> }}

```