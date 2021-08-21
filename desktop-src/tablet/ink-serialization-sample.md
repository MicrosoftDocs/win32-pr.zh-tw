---
description: 這個範例示範如何以各種格式序列化和還原序列化筆跡。
ms.assetid: 468d9c2a-0b3c-4a44-a049-3f3b78e952ba
title: 筆墨序列化範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80e71eed5c91bf4fa1524cc52af163516ced0c7362d0d20b8ecf52ac1a08ccd9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032266"
---
# <a name="ink-serialization-sample"></a>筆墨序列化範例

這個範例示範如何以各種格式序列化和還原序列化筆跡。 應用程式代表具有欄位的表單，可輸入名字、姓氏和簽章。 使用者可將此資料儲存為純筆墨序列化格式 (ISF) 、使用 base64 編碼的 ISF 來可延伸標記語言 (XML)  (XML) ，或使用 HTML 來參考 base64 編碼嚴加防禦中的筆跡圖形交換格式 (GIF) 影像。 應用程式也可讓使用者開啟儲存為 XML 和 ISF 格式的檔案。 ISF 格式會使用擴充屬性來儲存名字和姓氏，而 XML 和 HTML 格式會將這項資訊儲存在自訂屬性中。

此範例不支援從 HTML 格式載入，因為 HTML 不適合用來儲存結構化資料。 因為資料會分成名稱、簽章等，所以需要保留這種分隔的格式，例如 XML 或其他類型的資料庫格式。

HTML 在格式化很重要的環境中很有用，例如在文書處理檔中。 此範例所儲存的 HTML 會使用嚴加防禦 Gif。 這些 Gif 中內嵌了 ISF，可保留筆墨的完整精確度。 文書處理應用程式可以儲存包含多種資料類型的檔，例如影像、資料表、格式化的文字，以及以 HTML 格式保存的筆墨。 此 HTML 會在無法辨識筆墨的瀏覽器中轉譯。 不過，當載入已啟用筆墨的應用程式時，可以使用原始筆跡的完整精確度，並可加以轉譯、編輯或用於辨識。

此範例使用下列功能：

-   [筆墨](/previous-versions/aa515768(v=msdn.10))物件的[Load](/previous-versions/ms569609(v=vs.100))方法
-   [筆墨](/previous-versions/aa515768(v=msdn.10))物件的[Save](/previous-versions/dotnet/netframework-3.5/ms571335(v=vs.90))方法
-   [筆墨](/previous-versions/aa515768(v=msdn.10))物件的[ExtendedProperties](/previous-versions/ms582214(v=vs.100))屬性

## <a name="collecting-ink"></a>收集筆墨

首先，參考隨 Windows Vista 和 Windows XP Tablet pc Edition 軟體發展工具組 (SDK) 所安裝的 Tablet pc API。


```C++
using Microsoft.Ink;
```



此函式會建立並[](/previous-versions/ms836493(v=msdn.10))啟用 `ic` 表單的 InkCollector。


```C++
ic = new InkCollector(Signature.Handle);
ic.Enabled = true;
```



## <a name="saving-a-file"></a>儲存檔案

`SaveAsMenu_Click`方法會處理 [另存新檔] 對話方塊、建立用來儲存筆墨資料的檔案資料流程，以及呼叫對應至使用者選擇的儲存方法。

## <a name="saving-to-an-isf-file"></a>儲存至 ISF 檔案

在 `SaveISF` 方法中，第一個和最後一個名稱值會加入至[InkCollector](/previous-versions/ms836493(v=msdn.10))物件的[筆墨](/previous-versions/ms836505(v=msdn.10))屬性的[ExtendedProperties](/previous-versions/ms582214(v=vs.100))屬性，然後再將筆墨序列化並寫入檔案。 在將筆墨序列化之後，就會從 [ink](/previous-versions/aa515768(v=msdn.10)) 物件的 ExtendedProperties 屬性中移除第一個和最後一個名稱的值。


```C++
byte[] isf;

// This is the ink object which is serialized
ExtendedProperties inkProperties = ic.Ink.ExtendedProperties;

// Store the name fields in the ink object
// These fields roundtrip through the ISF format
// Ignore empty fields since strictly empty strings 
//       cannot be stored in ExtendedProperties.
if (FirstNameBox.Text.Length > 0)
{
    inkProperties.Add(FirstName, FirstNameBox.Text);
}
if (LastNameBox.Text.Length > 0)
{
    inkProperties.Add(LastName, LastNameBox.Text);
}

// Perform the serialization
isf = ic.Ink.Save(PersistenceFormat.InkSerializedFormat);

// If the first and last names were added as extended
// properties to the ink, remove them - these properties
// are only used for the save and there is no need to
// keep them around on the ink object.
if (inkProperties.DoesPropertyExist(FirstName))
{
    inkProperties.Remove(FirstName);
}
if (inkProperties.DoesPropertyExist(LastName))
{
    inkProperties.Remove(LastName);
}

// Write the ISF to the stream
s.Write(isf,0,isf.Length);
```



## <a name="saving-to-an-xml-file"></a>儲存至 XML 檔案

在 `SaveXML` 方法中， [XmlTextWriter](/dotnet/api/system.xml.xmltextwriter?view=netcore-3.1) 物件是用來建立和寫入 XML 檔。 使用 [筆墨](/previous-versions/aa515768(v=msdn.10)) 物件的 [Save](/previous-versions/dotnet/netframework-3.5/ms571335(v=vs.90)) 方法，會先將筆跡轉換為 base64 編碼的筆跡序列化格式位元組陣列，然後再將位元組陣列轉換成要寫出至 XML 檔案的字串。 表單中的文字資料也會寫出至 XML 檔案。


```C++
// Get the base64 encoded ISF
base64ISF_bytes = ic.Ink.Save(PersistenceFormat.Base64InkSerializedFormat);

// Convert it to a String
base64ISF_string = utf8.GetString(base64ISF_bytes);

// Write the ISF containing node to the XML
xwriter.WriteElementString("Ink", base64ISF_string);

// Write the text data from the form
// Note that the names are stored as XML fields, rather
// than custom properties, so that these properties can 
// be most easily accessible if the XML is saved in a database.
xwriter.WriteElementString("FirstName",FirstNameBox.Text);
xwriter.WriteElementString("LastName",LastNameBox.Text);
```



## <a name="saving-to-an-html-file"></a>儲存至 HTML 檔案

SaveHTML 方法會使用 [筆劃](/previous-versions/ms827799(v=msdn.10)) 集合的周框方塊來測試簽章是否存在。 如果簽章存在，則會使用筆墨物件的 [Save](/previous-versions/dotnet/netframework-3.5/ms571335(v=vs.90)) 方法，將它轉換成嚴加防禦 GIF 格式，並寫入檔案。 GIF 接著會在 HTML 檔案中參考。


```C++
if (ic.Ink.Strokes.GetBoundingBox().IsEmpty)
{
   MessageBox.Show("Unable to save empty ink in HTML persistence format.");
}
else
{
    FileStream gifFile;
    byte[] fortifiedGif = null;
    ...

    // Create a directory to store the fortified GIF which also contains ISF
    // and open the file for writing
    Directory.CreateDirectory(nameBase + "_files");
    using (FileStream gifFile = File.OpenWrite(nameBase + "_files\\signature.gif"))
    {

        // Generate the fortified GIF represenation of the ink
        fortifiedGif = ic.Ink.Save(PersistenceFormat.Gif);

        // Write and close the gif file
        gifFile.Write(fortifiedGif, 0, fortifiedGif.Length);
    }
```



## <a name="loading-a-file"></a>載入檔案

`OpenMenu_Click`方法會處理 [開啟] 對話方塊、開啟檔案，然後呼叫對應至使用者選擇的載入方法。

## <a name="loading-an-isf-file"></a>載入 ISF 檔案

`LoadISF`方法會讀取先前建立的檔案，並使用[筆墨](/previous-versions/aa515768(v=msdn.10))物件的[Load](/previous-versions/ms569609(v=vs.100))方法，將位元組陣列轉換為筆跡。 筆墨收集器已暫時停用，以將筆墨物件指派給它。 `LoadISF`然後，方法會檢查筆墨物件的[ExtendedProperties](/previous-versions/ms582214(v=vs.100))屬性，以取得第一個和最後一個名稱字串。


```C++
Ink loadedInk = new Ink();
byte[] isfBytes = new byte[s.Length];

// read in the ISF
s.Read(isfBytes, 0, (int) s.Length);

// load the ink into a new ink object
// After an ink object has been "dirtied" it can never load ink again
loadedInk.Load(isfBytes);

// temporarily disable the ink collector and swap ink objects
ic.Enabled = false;
ic.Ink = loadedInk;
ic.Enabled = true;

// Repaint the inkable region
Signature.Invalidate();

ExtendedProperties inkProperties = ic.Ink.ExtendedProperties;

// Get the raw data out of this stroke's extended
// properties list, using the previously defined 
// Guid as a key to the extended property.
// Since the save method stored the first and last
// name information as extended properties, this
// information can be remove now that the load is complete.
if (inkProperties.DoesPropertyExist(FirstName))
{
    FirstNameBox.Text = (String) inkProperties[FirstName].Data;
    inkProperties.Remove(FirstName);
}
else
{
    FirstNameBox.Text = String.Empty;
}

if (inkProperties.DoesPropertyExist(LastName))
{
    LastNameBox.Text = (String) inkProperties[LastName].Data;
    inkProperties.Remove(LastName);
}
else
{
    LastNameBox.Text = String.Empty;
}
```



## <a name="loading-an-xml-file"></a>載入 XML 檔案

`LoadXML`方法會載入先前建立的 XML 檔案、從筆墨節點抓取資料，然後使用[筆墨](/previous-versions/aa515768(v=msdn.10))物件的[Load](/previous-versions/ms569609(v=vs.100))方法，將節點中的資料轉換成筆墨。 暫時停用 [InkCollector](/previous-versions/ms836493(v=msdn.10)) ，將筆墨物件指派給它。 簽章方塊會失效，而第一個和最後一個名稱資訊則是從 XML 檔中取出。


```C++
// This object encodes our byte data to a UTF8 string
UTF8Encoding utf8 = new UTF8Encoding();

XmlDocument xd = new XmlDocument();
XmlNodeList nodes;
Ink loadedInk = new Ink();

// Load the XML data into a DOM
xd.Load(s);

// Get the data in the ink node
nodes = xd.GetElementsByTagName("Ink");

// load the ink into a new ink object
// After an ink object has been "dirtied" it can never load ink again
if (0 != nodes.Count)
    loadedInk.Load(utf8.GetBytes(nodes[0].InnerXml));

// temporarily disable the ink collector and swap ink objects
ic.Enabled = false;
ic.Ink = loadedInk;
ic.Enabled = true;

// Repaint the inkable region
Signature.Invalidate();

// Get the data in the FirstName node
nodes = xd.GetElementsByTagName("FirstName");
if (0 != nodes.Count)
{
    FirstNameBox.Text = nodes[0].InnerXml;
}
else
{
    FirstNameBox.Text = String.Empty;
}

// Get the data in the LastName node
nodes = xd.GetElementsByTagName("LastName");
if (0 != nodes.Count)
{
    LastNameBox.Text = nodes[0].InnerXml;
}
else
{
    LastNameBox.Text = String.Empty;
}
```



## <a name="closing-the-form"></a>關閉表單

表單的 [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) 方法會處置 [InkCollector](/previous-versions/ms836493(v=msdn.10)) 物件。

 

 
