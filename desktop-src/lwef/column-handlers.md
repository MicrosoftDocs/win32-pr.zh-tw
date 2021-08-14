---
title: 建立資料行處理常式
description: Windows Windows 檔案總管中的詳細資料檢視通常會顯示數個標準資料行。
ms.assetid: 805e0e13-d09e-40f8-955b-c585f388e07e
keywords:
- 資料行處理常式
- 註冊，資料行處理常式
- GetColumnInfo
- GetItemData
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90876aecdb2626326513723f0cd2c5a6e8f66bfd938b3f56cf10bd3624dd8687
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119349454"
---
# <a name="creating-column-handlers"></a>建立資料行處理常式

\[只有 Windows XP 或更早版本才支援這項功能。 \]

Windows Windows 檔案總管中的詳細資料檢視通常會顯示數個標準資料行。 每個資料行都會列出目前資料夾中每個檔案的資訊，例如檔案大小或類型。 藉由執行和註冊資料行處理常式，您可以讓自訂資料行可供顯示。

[建立 shell](/windows/desktop/shell/handlers)擴充處理常式時，會討論如何執行和註冊 shell 擴充處理常式的一般程式。 本檔著重于資料行處理常式特定的執行層面。

討論下列主題。

-   [資料行處理常式的運作方式](#how-column-handlers-work)
-   [註冊資料行處理常式](#registering-column-handlers)
-   [執行資料行處理常式](#implementing-column-handlers)
    -   [Initialize 方法](#the-initialize-method)
    -   [GetColumnInfo 方法](#the-getcolumninfo-method)
    -   [GetItemData 方法](#the-getitemdata-method)

## <a name="how-column-handlers-work"></a>資料行處理常式的運作方式

下圖顯示詳細資料檢視中的 Windows 檔案總管。

![詳細資料檢視中的 windows explorer 螢幕擷取畫面](images/columnproviderhandler1.jpg)

使用 Windows 2000 時，資料夾也可以支援一些預設不會顯示的資料行。 使用者可以在其中一個資料行標頭上按一下滑鼠右鍵，然後從功能表中選取 [ **其他 ...** ] 命令，以顯示其他資料行。 接著會出現一個對話方塊，列出資料夾可用的資料行，並讓使用者選取要顯示的資料行。 下圖顯示上述範例的這個對話方塊。

![顯示 [選擇詳細資料] 對話方塊的 windows explorer 螢幕擷取畫面](images/columnproviderhandler2.jpg)

藉由建立資料行處理常式，您可以建立自訂資料行，並將其加入至該清單。 例如，包含音樂的檔案集合可以使用資料行處理常式來顯示列出每個檔案所含之演出者和部分的資料行。

資料行處理常式是全域物件，會在每次 Windows 檔案總管顯示詳細資料檢視時呼叫。 不過，資料行處理常式通常只會用來顯示特定 [檔案類型](/windows/desktop/shell/fa-file-types)之成員的自訂資料行。 在顯示詳細資料檢視之前，Windows 檔案總管會針對其資料行特性查詢所有已註冊的資料行處理常式。 如果使用者已選取其中一個處理常式的資料行，Windows 檔案總管會查詢相關聯資料的處理常式。 當資料行處理常式收到資料的要求時，如果檔案是其支援類型的成員，則會提供資料。 否則，它會傳回 FALSE 來忽略要求 \_ 。

## <a name="registering-column-handlers"></a>註冊資料行處理常式

資料行處理常式會在下列子機碼下註冊。

```
HKEY_CLASSES_ROOT
   Folder
      shellex
         ColumnHandlers
```

使用處理程式的類別識別碼字串形式來建立名為 **ColumnHandlers** 的子機碼， (CLSID) GUID。 如需如何註冊 Shell 擴充處理常式的一般討論，請參閱 [建立 Shell 擴充處理](/windows/desktop/shell/handlers)程式。 下列範例說明如何註冊資料行處理常式。

```
HKEY_CLASSES_ROOT
   Folder
      shellex
         ColumnHandlers
            {My Column Handler CLSID GUID}
```

## <a name="implementing-column-handlers"></a>執行資料行處理常式

如同所有 Shell 延伸模組處理常式，資料行處理常式也是實作為 Dll (COM) 物件的同進程元件物件模型。 除了 [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)之外，它們還會匯出 [**IColumnProvider**](/windows/desktop/api/shlobj/nn-shlobj-icolumnprovider)介面。

WindowsExplorer 會呼叫 [**IColumnProvider**](/windows/desktop/api/shlobj/nn-shlobj-icolumnprovider)匯出的三個方法，以要求其顯示資料行所需的資訊。 Windows 檔案總管使用的程式如下：

1.  呼叫 [**IColumnProvider：： Initialize**](/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-initialize) 以指定即將顯示的資料夾。
2.  呼叫 [**IColumnProvider：： GetColumnInfo**](/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-getcolumninfo) ，以取得資料行的識別碼和特性。
3.  如果使用者已選取資料行，請為資料夾中的每個檔案呼叫 [**IColumnProvider：： GetItemData**](/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-getitemdata) ，以取出屬於檔案資料行專案的資料。

### <a name="the-initialize-method"></a>Initialize 方法

WindowsExplorer 會呼叫 [**IColumnProvider：： initialize**](/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-initialize)來初始化資料行處理常式。 方法有三個參數，但目前只使用 *wszFolder* 。 它會設定為要顯示其詳細資料檢視的資料夾。 儲存資料夾名稱以供稍後使用，並視需要初始化處理常式物件。

### <a name="the-getcolumninfo-method"></a>GetColumnInfo 方法

WindowsExplorer 接下來會呼叫 [**IColumnProvider：： GetColumnInfo**](/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-getcolumninfo)來要求資料行的識別碼和特性。 它會在 *dwIndex* 參數中傳遞資料行的索引。 此索引是用來列舉資料行的任意值。 WindowsExplorer 也會在 [**SHCOLUMNINFO**](/windows/desktop/api/shlobj/ns-shlobj-shcolumninfo)結構的指標中傳遞。 此結構是用來傳回資料行的識別碼和特性。 **IColumnProvider：： GetColumnInfo** 應該將適當的值指派給結構的成員，並傳回。

資料行是由其 OLE 屬性集識別碼 (FMTID) 和相關聯的屬性識別碼 (PID) 來識別。 [**SHCOLUMNINFO**](/windows/desktop/api/shlobj/ns-shlobj-shcolumninfo)結構（ **scid**）的第一個成員是用來識別資料行之 [**SHCOLUMNID**](/windows/desktop/shell/objects)結構的指標。 其 **fmtid** 成員會保留資料行的 fmtid，而其 **pid** 成員會保存該資料行的 pid。 例如，通常用來識別資料行的標準 FMTID/PID 組是摘要資訊屬性集的作者 PID。

可能的話，您的處理常式應該使用現有的 FMTIDs 和 Pid 來識別它所支援的資料行。 如果您使用自訂 [**SHCOLUMNID**](/windows/desktop/shell/objects) 結構，資料行會只顯示處理常式支援的那些檔案的資料。 如果資料夾包含其他檔案，其專案將會空白。 如果資料夾包含多個檔案類型的檔案，則使用標準 FMTID/PID 值可能會將不同類型的資料合併到相同的資料行中。

將 **vt** 成員設為您想要在資料行中顯示之資料的 [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) 類型。 最常使用的類型是 VT \_ LPSTR，因為大部分的資料行會以字元字串顯示其資料。 [**SHCOLUMNINFO**](/windows/desktop/api/shlobj/ns-shlobj-shcolumninfo)結構的其餘成員是用來定義資料行的特性。 適當地指派值。

### <a name="the-getitemdata-method"></a>GetItemData 方法

如果已選取資料行處理常式的資料行，Windows 檔案總管會針對要顯示之資料夾中的每個檔案呼叫 [**IColumnProvider：： GetItemData**](/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-getitemdata) 。 *Pscid* 參數是識別資料行之 [**SHCOLUMNID**](/windows/desktop/shell/objects)結構的指標。 *Pscd* 參數指向識別特定檔案的 [**SHCOLUMNDATA**](/windows/desktop/api/shlobj/ns-shlobj-shcolumndata)結構。

*PvarData* 參數會傳回應該在 *pscd* 所指定檔案的處理常式資料行中顯示的資料。 如果您的資料行處理常式支援該檔案，請將其資料值指派給 *pvarData* ，然後返回 S \_ OK。 如果您的資料行處理常式不支援此檔案，則傳回 \_ FALSE，而不將值指派給 *pvarData*。

許多資料夾會包含任何特定資料行處理常式不支援的一些檔案。 為了提高效率， [**IColumnProvider：： GetItemData**](/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-getitemdata)應該先檢查 *pscd* 所指向之結構的 **pwszExt** 成員。 這個成員會保留副檔名。 如果延伸模組指出檔案不是您的處理常式所支援之檔案類型的成員，請立即傳回 FALSE，以避免不必要的處理 \_ 。

 

 