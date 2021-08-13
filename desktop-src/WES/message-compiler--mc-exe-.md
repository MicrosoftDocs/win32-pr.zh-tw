---
title: '訊息編譯器 (MC.exe) '
description: 用來編譯檢測資訊清單和訊息文字檔。
ms.assetid: f9de35f1-6d31-4f4b-b2c4-8474d6fce9e0
keywords:
- 訊息編譯器 (MC.exe) EventLog
topic_type:
- apiref
api_name:
- Message Compiler (MC.exe)
api_type:
- NA
ms.topic: reference
ms.date: 06/03/2020
ms.openlocfilehash: 1ba213a1d7047b61ba7ba875adf9c281726eaae123ae018aea9920050b201644
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119470938"
---
# <a name="message-compiler-mcexe"></a>訊息編譯器 (MC.exe) 

用來編譯檢測資訊清單和訊息文字檔。 編譯器會產生您的應用程式所連結的訊息資源檔。

``` syntax
MC [-?aAbcdnouUv] [-m <length>] [-h <path>] [-e <extension>] [-r <path>]
   [-x <path>] [-w <file>] [-W <file>] [-z <basename> ] [-cp <encoding>]
   [-km | -um | -generateProjections | -cs <namespace>]
   [-mof] [-p <prefix>] [-P <prefix>]
   [<filename.man>] [<filename.mc>]
```

-   [訊息文字檔與資訊清單檔案通用的引數](#arguments-common-to-both-message-text-files-and-manifest-files)
-   [資訊清單檔特定的引數](#arguments-specific-to-manifest-files)
-   [產生提供者用來記錄事件之程式碼的特定引數](#arguments-specific-to-generating-code-that-your-provider-would-use-to-log-events)
-   [訊息文字檔特定的引數](#arguments-specific-to-message-text-files)

## <a name="arguments-common-to-both-message-text-files-and-manifest-files"></a>訊息文字檔與資訊清單檔案通用的引數

<dl> <dt>

<span id="-_"></span>**-?**
</dt> <dd>

顯示訊息編譯器的使用量資訊。

</dd> <dt>

<span id="-c"></span><span id="-C"></span>**-c**
</dt> <dd>

使用這個引數，讓編譯器將客戶位設定為在所有訊息識別碼中 (位 28) 。 如需客戶位的詳細資訊，請參閱 winerror.h。

</dd> <dt>

<span id="-cp"></span><span id="-CP"></span>**-cp** *編碼*
</dt> <dd>

您可以使用這個引數來指定用於所有產生之文字檔的字元編碼。 有效的名稱包括「ansi」 (預設) 、「utf-8」和「utf-16」。 Unicode 編碼會加入位元組順序標記。

</dd> <dt>

<span id="-e_extension"></span><span id="-E_EXTENSION"></span>**-e** *擴充* 功能
</dt> <dd>

使用這個引數來指定要用於標頭檔的延伸模組。 您最多可以指定三個字元的副檔名，而不包含句點。 預設值為 .h。

</dd> <dt>

<span id="-h_path"></span><span id="-H_PATH"></span>**-h** *路徑*
</dt> <dd>

您可以使用這個引數來指定要編譯器放置所產生標頭檔的資料夾。 預設值是目前的目錄。

</dd> <dt>

<span id="-m_length"></span><span id="-M_LENGTH"></span>**-m** *長度*
</dt> <dd>

使用這個引數可讓編譯器在任何訊息超過 *長度* 字元時產生警告。

</dd> <dt>

<span id="-r_path"></span><span id="-R_PATH"></span>**-r** *路徑*
</dt> <dd>

您可以使用這個引數來指定要編譯器將產生的資源編譯器腳本放 ( .rc 檔) 和產生的 bin 檔案 (二進位資源的資料夾，) 資源編譯器腳本所包含的檔案。 預設值是目前的目錄。

</dd> <dt>

<span id="-z_name"></span><span id="-Z_NAME"></span>**-z** *名稱*
</dt> <dd>

使用這個引數來覆寫編譯器針對其產生的檔案所使用的預設基底名稱。 預設值是使用 *檔案名* 輸入檔的基底名稱。

</dd> <dt>

<span id="filename"></span><span id="FILENAME"></span>*檔案名*
</dt> <dd>

檢測資訊清單檔案或訊息文字檔。 檔案必須存在於目前的目錄中。 您可以指定資訊清單檔、訊息文字檔或兩者。 檔案名必須包含副檔名。 慣例是在資訊清單檔中使用 man 副檔名，並為郵件文字檔使用 mc 副檔名。

</dd> </dl>

### <a name="arguments-specific-to-manifest-files"></a>資訊清單檔特定的引數

<dl> <dt>

<span id="-s_path"></span><span id="-S_PATH"></span>**-s** *路徑*
</dt> <dd>

使用這個引數來建立您的檢測基準。 指定包含您的基準資訊清單檔案之資料夾的路徑。 在後續的版本中，您會使用 **-t** 引數，根據相容性問題的基準來檢查新的資訊清單。

**在 MC 版本1.12.7051 之前：** 無法使用

</dd> <dt>

<span id="-t_path"></span><span id="-T_PATH"></span>**-t** *路徑*
</dt> <dd>

當您建立新版本的資訊清單，而且想要檢查它是否符合您使用 **-s** 引數所建立的基準時，請使用這個引數。 路徑必須指向包含的資料夾。基準作業所建立的 BIN 檔案 (看到 **-s** 參數) 。

**在 MC 版本1.12.7051 之前：** 無法使用

</dd> <dt>

<span id="-w_path"></span><span id="-W_PATH"></span>**-w** *路徑*
</dt> <dd>

編譯器會忽略此引數，並自動驗證資訊清單。

**在 MC 版本1.12.7051 之前：** 您可以使用這個引數來指定包含 Eventman .xsd 架構檔案的資料夾，而編譯器會使用此檔案來驗證您的資訊清單。 Windows SDK 在 Include 資料夾中包含 Eventman .xsd 架構檔案。 \\ 如果您未指定這個引數，則編譯器不會驗證您的資訊清單。

</dd> <dt>

<span id="-W_path"></span><span id="-w_path"></span><span id="-W_PATH"></span>**-W** *路徑*
</dt> <dd>

編譯器會忽略此引數。

**在 MC 版本1.12.7051 之前：** 使用這個引數來指定包含 Winmeta.xml 檔的資料夾。 Winmeta.xml 檔案包含已辨識的輸入和輸出類型，以及預先定義的通道、層級和 opcode。 Windows SDK 包含包含資料夾中的 Winmeta.xml 檔案 \\ 。

</dd> </dl>

### <a name="arguments-specific-to-generating-code-that-your-provider-would-use-to-log-events"></a>產生提供者用來記錄事件之程式碼的特定引數

您可以使用下列編譯器引數來產生核心模式或使用者模式程式碼，您可以用來記錄事件。 您也可以要求編譯器產生程式碼，以支援在 Windows Vista 之前將事件寫入電腦上。 如果您的應用程式是以 c # 撰寫，則編譯器可以產生可供您用來記錄事件的 c # 類別。 從 windows SDK Windows 7 版隨附的 MC 版本1.12.7051 開始，可以使用這些引數。

<dl> <dt>

<span id="-co"></span><span id="-CO"></span>**-co**
</dt> <dd>

您可以使用這個引數，讓記錄服務針對您所記錄的每個事件呼叫您的使用者定義函數， (在) 事件記錄之後呼叫該函式。 您的使用者定義函數必須有下列簽章。


```C++
VOID
pFnUserFunction(
    __in REGHANDLE RegHandle,
    __in PCEVENT_DESCRIPTOR Descriptor,
    __in ULONG EventDataCount,
    __in_ecount(EventDataCount) PEVENT_DATA_DESCRIPTOR EventData
    );
```



您也必須在程式碼中包含下列指示詞。

`#define MCGEN_CALLOUT pFnUserFunction`

您應盡可能縮短您的執行，以避免記錄問題;在函數傳回之前，服務將不會再記錄您的事件。

您可以使用這個引數搭配 **-公里** 或 **-um** 引數。

</dd> <dt>

<span id="-cs_namespace"></span><span id="-CS_NAMESPACE"></span>**-cs** *命名空間*
</dt> <dd>

您可以使用這個引數，讓編譯器根據 .NET 3.5 [EventProvider](/dotnet/api/system.diagnostics.eventing.eventprovider?view=netframework-3.5&preserve-view=true) 類別產生 c # 類別。

</dd> <dt>

<span id="-css_namespace"></span><span id="-CSS_NAMESPACE"></span>**-css** *命名空間*
</dt> <dd>

您可以使用這個引數，讓編譯器根據 .NET 3.5 [EventProvider](/dotnet/api/system.diagnostics.eventing.eventprovider?view=netframework-3.5&preserve-view=true) 類別產生靜態 c # 類別。

</dd> <dt>

<span id="-km"></span><span id="-KM"></span>**-公里**
</dt> <dd>

您可以使用這個引數，讓編譯器產生核心模式程式碼，用來記錄資訊清單中所定義的事件。

</dd> <dt>

<span id="-mof"></span><span id="-MOF"></span>**-mof**
</dt> <dd>

廢棄。 您可以使用這個引數，讓編譯器產生程式碼，以便在 Windows Vista 之前將事件記錄到電腦上。 此選項也會建立一個 MOF 檔案，其中包含資訊清單中所定義之每個事件的 MOF 類別。 若要註冊 MOF 檔案中的類別，讓取用者可以解碼事件，請使用 MOF 編譯器 (Mofcomp.exe) 。 如需使用 MOF 編譯器的詳細資訊，請參閱 [受控物件格式](/windows/desktop/WmiSdk/managed-object-format--mof-)。

若要使用此參數，您必須遵守下列限制：

-   每個事件定義都必須包含工作和 opcode 屬性
-   每項工作都必須包含 eventGuid 屬性
-   事件所參考的範本資料不能包含：
    -   指定 win： Binary 或 win： SYSTEMTIME 輸入類型的資料項目
    -   結構
    -   變數大小的陣列;不過，您可以指定固定長度的陣列
    -   字串資料類型無法指定長度屬性

您必須使用此引數搭配 **-um**、 **-cs**、 **-css** 或 **-公里** 引數

</dd> <dt>

<span id="-p_prefix"></span><span id="-P_PREFIX"></span>**-p** *前置* 詞
</dt> <dd>

使用這個引數來覆寫編譯器用來記錄宏名稱和方法名稱的預設前置詞。 預設前置詞是 "EventWrite"。 此字串區分大小寫。

您可以使用這個引數搭配 **-um**、 **-cs**、 **-css** 或 **-公里** 引數。

</dd> <dt>

<span id="-P_prefix"></span><span id="-p_prefix"></span><span id="-P_PREFIX"></span>**-P** *前置* 詞
</dt> <dd>

使用這個引數，從您為事件指定的符號名稱開頭移除字元。 此比較不區分大小寫。 編譯器會使用符號名稱來構成記錄宏名稱和方法名稱。

記錄宏的預設名稱是 EventWrite *SymbolName*，其中 *SymbolName* 是您為事件指定的符號名稱。 例如，如果您將事件的 symbol 屬性設為 PrinterConnection，則宏名稱會是 EventWritePrinterConnection。 若要從名稱移除印表機，請使用 **-P** **印表機**，這會導致 EventWriteConnection。

您可以使用這個引數搭配 **-um**、 **-cs**、 **-css** 或 **-公里** 引數。

</dd> <dt>

<span id="-um"></span><span id="-UM"></span>**-um**
</dt> <dd>

您可以使用這個引數，讓編譯器產生使用者模式程式碼，用來記錄您在資訊清單中定義的事件。

</dd> </dl>

若要讓編譯器產生記錄程式碼，您必須指定 **-um**、 **-cs**、 **-css** 或 **-公里** 引數;這些引數都是互斥的。

若要指定編譯器所產生之 .h、.cs 和 mof 檔案的放置位置，請使用 **-h** 引數。 如果您未指定 **-h** 引數，則會將檔案放在目前的資料夾中。

若要指定要將 .rc 檔和二進位檔案放 (的位置，其中包含編譯器所產生) 的中繼資料資源，請使用 **-r** 引數。 如果您未指定 **-r** 引數，則會將檔案放在目前的資料夾中。

編譯器會使用輸入檔的基底名稱做為它所產生之檔案的基底名稱。 若要指定基底名稱，請使用 **-z** 引數。

### <a name="arguments-specific-to-message-text-files"></a>訊息文字檔特定的引數

<dl> <dt>

<span id="-a"></span><span id="-A"></span>**-a**
</dt> <dd>

使用這個引數來指定 *檔案名* 輸入檔包含系統預設 Windows ANSI 字碼頁中的內容 (CP_ACP) 。 此為預設值。 使用 **-u** 代表 Unicode。 如果輸入檔包含 BOM，則會忽略此引數。

</dd> <dt>

<span id="-A"></span><span id="-a"></span>**-A**
</dt> <dd>

廢棄。 使用這個引數來指定輸出 bin 檔案中的訊息應該是 ANSI。

</dd> <dt>

<span id="-b"></span><span id="-B"></span>**-b**
</dt> <dd>

您可以使用這個引數，讓編譯器使用 *檔案名* 輸入檔的基底名稱作為 bin 檔案名。 預設值是使用 "MSG"。

</dd> <dt>

<span id="-d"></span><span id="-D"></span>**-d.ddd...e**
</dt> <dd>

使用這個引數可針對標頭檔中的嚴重性和設備常數使用十進位值，而不是使用十六進位值。

</dd> <dt>

<span id="-n"></span><span id="-N"></span>**-n**
</dt> <dd>

使用這個引數來指定訊息在訊息本文之後立即終止。 預設值是使用 CR/LF 來終止訊息主體。

</dd> <dt>

<span id="-o"></span><span id="-O"></span>**-o**
</dt> <dd>

您可以使用這個引數，讓編譯器使用 **HRESULT** 定義來產生 OLE2 標頭檔，而不是狀態碼。 預設會使用狀態碼。

</dd> <dt>

<span id="-u"></span><span id="-U"></span>**-u**
</dt> <dd>

使用這個引數來指定 *檔案名* 輸入檔案包含 utf-16le 內容。 預設值為 ANSI 內容。 如果輸入檔包含 BOM，則會忽略此引數。

</dd> <dt>

<span id="-U"></span><span id="-u"></span>**-U**
</dt> <dd>

使用這個引數來指定輸出 bin 檔案中的訊息應該是 Unicode。 此為預設值。

</dd> <dt>

<span id="-v"></span><span id="-V"></span>**-v**
</dt> <dd>

使用這個引數以產生詳細資訊輸出。

</dd> <dt>

<span id="-x_path"></span><span id="-X_PATH"></span>**-x** *路徑*
</dt> <dd>

您可以使用這個引數來指定您要編譯器放置 dbg C include 檔的資料夾。 此 dbg 檔案會將訊息識別碼對應至其符號名稱。

</dd> </dl>

## <a name="remarks"></a>備註

**-A** 和 **-mof** 引數已淘汰，未來將會移除。

編譯器會將資訊清單接受為輸入 ( 的) 檔案或郵件內文 ( mc) 檔案，並產生下列檔案：

-   *filename*。h

    C/c + + 標頭檔，其中包含您在應用程式中參考的事件描述元、提供者 GUID 和符號名稱。

-   *檔案名* 臨時 bin

    包含提供者和事件中繼資料的二進位資源檔。 這是範本資源，以檔案基底名稱的暫存尾碼表示。

-   Msg00001 bin

    您所指定之每種語言的二進位資源檔 (例如，如果您的資訊清單包含 en-us 和 fr-fr 中的訊息字串，則編譯器會產生 Msg00001 bin 和 Msg00002) 。

-   *檔案名*.rc

    資源編譯器腳本，其中包含要包含每個 bin 檔案做為資源的語句。

若為採用路徑的引數，路徑可以是絕對路徑、相對路徑或 UNC 路徑，而且可以包含環境變數。

**在 MC 版本1.12.7051 之前：** 編譯器不允許相對路徑或環境變數。

Windows SDK 包含 Bin 資料夾中的編譯器 (mc.exe) \\ 。

## <a name="examples"></a>範例

下列範例會使用編譯器預設值來編譯資訊清單。

``` syntax
mc spooler.man
```

下列範例會編譯資訊清單，並將標頭和資源檔放在指定的資料夾中。

``` syntax
mc -h <pathgoeshere> -r <pathgoeshere> spooler.man
```

## <a name="requirements"></a>規格需求

| 需求 | 值 |
|--------------------------|-------------------------------------------------|
| 最低支援的用戶端 | Windows 2000 Professional \[僅限傳統型應用程式\] |
| 最低支援的伺服器 | Windows 2000 Server \[僅限傳統型應用程式\]       |
