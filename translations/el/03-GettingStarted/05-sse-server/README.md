<!--
CO_OP_TRANSLATOR_METADATA:
{
  "original_hash": "1681ca3633aeb49ee03766abdbb94a93",
  "translation_date": "2025-06-17T22:12:55+00:00",
  "source_file": "03-GettingStarted/05-sse-server/README.md",
  "language_code": "el"
}
-->
Τώρα που γνωρίζουμε λίγα περισσότερα για το SSE, ας δημιουργήσουμε έναν SSE server.

## Άσκηση: Δημιουργία SSE Server

Για να δημιουργήσουμε τον server, πρέπει να έχουμε στο μυαλό μας δύο πράγματα:

- Πρέπει να χρησιμοποιήσουμε έναν web server για να εκθέσουμε endpoints για τη σύνδεση και τα μηνύματα.
- Να χτίσουμε τον server μας όπως συνήθως, με εργαλεία, πόρους και prompts όπως κάναμε με το stdio.

### -1- Δημιουργία instance server

Για να δημιουργήσουμε τον server, χρησιμοποιούμε τους ίδιους τύπους όπως με το stdio. Ωστόσο, για το transport, πρέπει να επιλέξουμε SSE.

---

Ας προσθέσουμε τώρα τις απαραίτητες διαδρομές.

### -2- Προσθήκη διαδρομών

Προσθέτουμε διαδρομές που διαχειρίζονται τη σύνδεση και τα εισερχόμενα μηνύματα:

---

Ας προσθέσουμε τώρα λειτουργίες στον server.

### -3- Προσθήκη λειτουργιών στον server

Τώρα που έχουμε ορίσει τα πάντα ειδικά για το SSE, ας προσθέσουμε λειτουργίες όπως εργαλεία, prompts και πόρους.

---

Ο πλήρης κώδικάς σας θα πρέπει να μοιάζει ως εξής:

---

Τέλεια, έχουμε έναν server που χρησιμοποιεί SSE, ας τον δοκιμάσουμε τώρα.

## Άσκηση: Εντοπισμός σφαλμάτων SSE Server με Inspector

Το Inspector είναι ένα εξαιρετικό εργαλείο που είδαμε σε προηγούμενο μάθημα [Δημιουργία του πρώτου σας server](/03-GettingStarted/01-first-server/README.md). Ας δούμε αν μπορούμε να το χρησιμοποιήσουμε και εδώ:

### -1- Εκτέλεση του inspector

Για να τρέξετε τον inspector, πρέπει πρώτα να έχετε έναν SSE server σε λειτουργία, οπότε ας το κάνουμε τώρα:

1. Εκτελέστε τον server

---

1. Εκτελέστε τον inspector

    > ![NOTE]
    > Τρέξτε αυτό σε ξεχωριστό παράθυρο τερματικού από αυτό που τρέχει ο server. Επίσης, σημειώστε ότι πρέπει να προσαρμόσετε την παρακάτω εντολή ώστε να ταιριάζει με το URL όπου τρέχει ο server σας.

    ```sh
    npx @modelcontextprotocol/inspector --cli http://localhost:8000/sse --method tools/list
    ```

    Η εκτέλεση του inspector είναι ίδια σε όλα τα περιβάλλοντα εκτέλεσης. Παρατηρήστε πως αντί να δίνουμε μια διαδρομή για τον server και μια εντολή εκκίνησης, περνάμε το URL όπου τρέχει ο server και επίσης ορίζουμε τη διαδρομή `/sse`.

### -2- Δοκιμή του εργαλείου

Συνδεθείτε στον server επιλέγοντας SSE από το αναπτυσσόμενο μενού και συμπληρώστε το πεδίο URL όπου τρέχει ο server σας, π.χ. http:localhost:4321/sse. Τώρα κάντε κλικ στο κουμπί "Connect". Όπως πριν, επιλέξτε να εμφανιστούν τα εργαλεία, επιλέξτε ένα εργαλείο και δώστε τις τιμές εισόδου. Θα δείτε ένα αποτέλεσμα όπως το παρακάτω:

![SSE Server running in inspector](../../../../translated_images/sse-inspector.d86628cc597b8fae807a31d3d6837842f5f9ee1bcc6101013fa0c709c96029ad.el.png)

Τέλεια, μπορείτε να δουλέψετε με τον inspector, ας δούμε τώρα πώς μπορούμε να δουλέψουμε με το Visual Studio Code.

## Ανάθεση

Προσπαθήστε να επεκτείνετε τον server σας με περισσότερες λειτουργίες. Δείτε [αυτή τη σελίδα](https://api.chucknorris.io/) για παράδειγμα, για να προσθέσετε ένα εργαλείο που καλεί ένα API. Εσείς αποφασίζετε πώς θα είναι ο server. Καλή διασκέδαση :)

## Λύση

[Λύση](./solution/README.md) Εδώ είναι μια πιθανή λύση με λειτουργικό κώδικα.

## Βασικά Συμπεράσματα

Τα βασικά σημεία που πρέπει να κρατήσετε από αυτό το κεφάλαιο είναι τα εξής:

- Το SSE είναι το δεύτερο υποστηριζόμενο transport μετά το stdio.
- Για να υποστηρίξετε SSE, πρέπει να διαχειρίζεστε εισερχόμενες συνδέσεις και μηνύματα χρησιμοποιώντας ένα web framework.
- Μπορείτε να χρησιμοποιήσετε τόσο τον Inspector όσο και το Visual Studio Code για να καταναλώσετε έναν SSE server, όπως και με τους stdio servers. Παρατηρήστε πως διαφέρει λίγο ανάμεσα σε stdio και SSE. Για το SSE, πρέπει να ξεκινήσετε τον server ξεχωριστά και μετά να τρέξετε το εργαλείο inspector. Επίσης, για το εργαλείο inspector, υπάρχουν κάποιες διαφορές καθώς πρέπει να ορίσετε το URL.

## Παραδείγματα

- [Java Calculator](../samples/java/calculator/README.md)
- [.Net Calculator](../../../../03-GettingStarted/samples/csharp)
- [JavaScript Calculator](../samples/javascript/README.md)
- [TypeScript Calculator](../samples/typescript/README.md)
- [Python Calculator](../../../../03-GettingStarted/samples/python)

## Επιπλέον Πόροι

- [SSE](https://developer.mozilla.org/en-US/docs/Web/API/Server-sent_events)

## Τι Ακολουθεί

- Επόμενο: [HTTP Streaming με MCP (Streamable HTTP)](/03-GettingStarted/06-http-streaming/README.md)

**Αποποίηση ευθυνών**:  
Αυτό το έγγραφο έχει μεταφραστεί χρησιμοποιώντας την υπηρεσία αυτόματης μετάφρασης AI [Co-op Translator](https://github.com/Azure/co-op-translator). Παρότι προσπαθούμε για ακρίβεια, παρακαλούμε να έχετε υπόψη ότι οι αυτόματες μεταφράσεις ενδέχεται να περιέχουν λάθη ή ανακρίβειες. Το πρωτότυπο έγγραφο στη γλώσσα του θεωρείται η αυθεντική πηγή. Για κρίσιμες πληροφορίες, συνιστάται επαγγελματική ανθρώπινη μετάφραση. Δεν φέρουμε ευθύνη για τυχόν παρεξηγήσεις ή λανθασμένες ερμηνείες που προκύπτουν από τη χρήση αυτής της μετάφρασης.