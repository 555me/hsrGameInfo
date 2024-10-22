# SRData
Repository containing the data for the game HSR.

# How do I find the missing text map entries?

```csharp
public static int GetStableHash(string str) {
    unchecked {
        int hash1 = 5381;
        int hash2 = hash1;

        for (int i = 0; i < str.Length && str[i] != '\0'; i += 2) {
            hash1 = ((hash1 << 5) + hash1) ^ str[i];
            if (i == str.Length - 1 || str[i + 1] == '\0')
                break;
            hash2 = ((hash2 << 5) + hash2) ^ str[i + 1];
        }

        return (hash1 + (hash2 * 1566083941));
    }
}
```

## This repository forks [Dim](https://github.com/Dimbreath) on gitlab.Thank you for providing the data.