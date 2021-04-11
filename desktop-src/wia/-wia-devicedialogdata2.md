---
description: 定義呼叫裝置對話方塊所需的資料。
ms.assetid: 544238de-310f-4fc3-b519-bb4e6b309272
title: 'DEVICEDIALOGDATA2 結構 (Wiadefd .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DEVICEDIALOGDATA2
api_type:
- HeaderDef
api_location:
- Wiadefd.h
ms.openlocfilehash: f4ab56114054b4f69a21fd9f4c05a1e119bab5da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026771"
---
# <a name="devicedialogdata2-structure"></a>DEVICEDIALOGDATA2 結構

定義呼叫裝置對話方塊所需的資料。

## <a name="syntax"></a>語法


```C++
typedef struct {
  DWORD     cbSize;
  IWiaItem2 *pIWiaItemRoot;
  DWORD     dwFlags;
  HWND      hwndParent;
  BSTR      bstrFolderName;
  BSTR      bstrFilename;
  LONG      lNumFiles;
  BSTR      *pbstrFilePaths;
  IWiaItem2 *ppWiaItem;
} DEVICEDIALOGDATA2;
```



## <a name="members"></a>成員

<dl> <dt>

**cbSize**
</dt> <dd>

類型： **DWORD**

</dd> <dd>

指定此結構的大小（以位元組為單位）。

</dd> <dt>

**pIWiaItemRoot**
</dt> <dd>

類型： **[**IWiaItem2**](-wia-iwiaitem2.md) \** _

</dd> <dd>

指向 [_ *IWiaItem2* *](-wia-iwiaitem2.md)介面，表示應用程式專案樹狀結構中的有效根專案。

</dd> <dt>

**dwFlags**
</dt> <dd>

類型： **DWORD**

</dd> <dd>

指定一組旗標來控制對話方塊的操作。 可以設定為下列任何值：



| 旗標                                 | 意義                                                                                                                                                                                     |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0                                    | 預設行為。                                                                                                                                                                           |
| WIA \_ 裝置 \_ 對話方塊 \_ 單一 \_ 影像   | 在 [裝置映射取得] 對話方塊中，將影像選取範圍限制為單一影像。                                                                                                      |
| WIA \_ 裝置 \_ 對話方塊 \_ 使用 \_ 一般 \_ UI | 使用系統 UI （如果有的話），而不是廠商提供的 UI。 如果系統 UI 無法使用，則會使用廠商 UI。 如果沒有可用的 UI，函數會傳回 E \_ >notimpl。 |



 

</dd> <dt>

**hwndParent**
</dt> <dd>

類型： **HWND**

</dd> <dd>

指定對話方塊父視窗的控制碼。

</dd> <dt>

**bstrFolderName**
</dt> <dd>

類型： **BSTR**

</dd> <dd>

指定要傳送檔案的資料夾名稱。

</dd> <dt>

**bstrFilename**
</dt> <dd>

類型： **BSTR**

</dd> <dd>

指定要用於從 WIA 專案傳輸至 **bstrFolderName** 所指定目的資料夾之檔案的檔案名範本。 您可以將額外的字元附加至檔案名範本，以建立任意數目的唯一檔案名。

</dd> <dt>

**lNumFiles**
</dt> <dd>

類型： **LONG**

</dd> <dd>

接收寫入至 **pbstrFilePaths** 陣列的字串數目。

</dd> <dt>

**pbstrFilePaths**
</dt> <dd>

類型： **BSTR \** _

</dd> <dd>

指向 BSTR 指標陣列的指標。 每個陣列元素都會指向一個 BSTR，其中包含已成功傳送至 bstrFolderName 所識別之資料夾的檔案目的地名稱。 方法必須配置這個成員的儲存體。

</dd> <dt>

_ *ppWiaItem**
</dt> <dd>

類型： **[**IWiaItem2**](-wia-iwiaitem2.md) \** _

</dd> <dd>

WIA 專案的 [_ *IWiaItem2* *](-wia-iwiaitem2.md)介面指標，該專案會將資料傳輸至 **pbstrFilePaths** 陣列中所命名的檔案。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>Wiadefd。h</dt> </dl> |



 

 




