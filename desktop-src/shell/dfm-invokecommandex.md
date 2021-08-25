---
description: 由預設內容功能表程式傳送至要求 LPFNDFMCALLBACK，以叫用擴充的功能表命令。
title: 'DFM_INVOKECOMMANDEX 訊息 (Shlobj.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 6ef885e5-2ddd-4a1b-9f8e-016a74e292b1
api_name:
- DFM_INVOKECOMMANDEX
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2b8a7fd63aa4269ee265a4ae147c99fe394e8aad725f7134f8d62daf8ee9984b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119943168"
---
# <a name="dfm_invokecommandex-message"></a>DFM \_ INVOKECOMMANDEX 訊息

由預設內容功能表程式傳送至要求 [**LPFNDFMCALLBACK**](/windows/win32/api/shlobj_core/nc-shlobj_core-lpfndfmcallback) ，以叫用擴充的功能表命令。


```C++
                DFM_INVOKECOMMANDEX
    wParam = (WPARAM)(int) idCmd;           
    lParam = (LPARAM)(DFMICS) PDFMICS;
            
```



## <a name="parameters"></a>參數

<dl> <dt>

*idCmd* \[\]
</dt> <dd>

所選功能表命令的命令識別碼。 可辨識下列旗標。

<dt>

<span id="DFM_CMD_DELETE"></span><span id="dfm_cmd_delete"></span>

<span id="DFM_CMD_DELETE"></span><span id="dfm_cmd_delete"></span>**DFM \_ CMD \_ DELETE**


</dt> <dd></dd> <dt>

<span id="DFM_CMD_MOVE"></span><span id="dfm_cmd_move"></span>

<span id="DFM_CMD_MOVE"></span><span id="dfm_cmd_move"></span>**DFM \_ CMD \_ 移動**


</dt> <dd></dd> <dt>

<span id="DFM_CMD_COPY"></span><span id="dfm_cmd_copy"></span>

<span id="DFM_CMD_COPY"></span><span id="dfm_cmd_copy"></span>**DFM \_ CMD \_ 複製**


</dt> <dd></dd> <dt>

<span id="DFM_CMD_LINK"></span><span id="dfm_cmd_link"></span>

<span id="DFM_CMD_LINK"></span><span id="dfm_cmd_link"></span>**DFM \_ CMD \_ 連結**


</dt> <dd></dd> <dt>

<span id="DFM_CMD_PROPERTIES"></span><span id="dfm_cmd_properties"></span>

<span id="DFM_CMD_PROPERTIES"></span><span id="dfm_cmd_properties"></span>**DFM \_ CMD \_ 屬性**


</dt> <dd>

顯示在其上叫用功能表之專案的 [ **屬性** ] UI。

</dd> <dt>

<span id="DFM_CMD_NEWFOLDER"></span><span id="dfm_cmd_newfolder"></span>

<span id="DFM_CMD_NEWFOLDER"></span><span id="dfm_cmd_newfolder"></span>**DFM \_ CMD \_ NEWFOLDER**


</dt> <dd></dd> <dt>

<span id="DFM_CMD_PASTE"></span><span id="dfm_cmd_paste"></span>

<span id="DFM_CMD_PASTE"></span><span id="dfm_cmd_paste"></span>**DFM \_ CMD \_ 貼上**


</dt> <dd></dd> <dt>

<span id="DFM_CMD_VIEWLIST"></span><span id="dfm_cmd_viewlist"></span>

<span id="DFM_CMD_VIEWLIST"></span><span id="dfm_cmd_viewlist"></span>**DFM \_ CMD \_ VIEWLIST**


</dt> <dd></dd> <dt>

<span id="DFM_CMD_VIEWDETAILS"></span><span id="dfm_cmd_viewdetails"></span>

<span id="DFM_CMD_VIEWDETAILS"></span><span id="dfm_cmd_viewdetails"></span>**DFM \_ CMD \_ VIEWDETAILS**


</dt> <dd></dd> <dt>

<span id="DFM_CMD_PASTELINK"></span><span id="dfm_cmd_pastelink"></span>

<span id="DFM_CMD_PASTELINK"></span><span id="dfm_cmd_pastelink"></span>**DFM \_ CMD \_ PASTELINK**


</dt> <dd></dd> <dt>

<span id="DFM_CMD_PASTESPECIAL"></span><span id="dfm_cmd_pastespecial"></span>

<span id="DFM_CMD_PASTESPECIAL"></span><span id="dfm_cmd_pastespecial"></span>**DFM \_ CMD \_ PASTESPECIAL**


</dt> <dd></dd> <dt>

<span id="DFM_CMD_MODALPROP"></span><span id="dfm_cmd_modalprop"></span>

<span id="DFM_CMD_MODALPROP"></span><span id="dfm_cmd_modalprop"></span>**DFM \_ CMD \_ MODALPROP**


</dt> <dd></dd> <dt>

<span id="DFM_CMD_RENAME"></span><span id="dfm_cmd_rename"></span>

<span id="DFM_CMD_RENAME"></span><span id="dfm_cmd_rename"></span>**DFM \_ CMD \_ 重新命名**


</dt> <dd></dd> </dl> </dd> <dt>

*PDFMICS* \[在\]
</dt> <dd>

[**DFMICS**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dfmics)結構的指標，其中包含所選功能表命令的其他引數。 此參數可以是 **Null**。

</dd> </dl>

## <a name="remarks"></a>備註

收到此訊息時， \_ 如果您想要讓預設的實值叫用命令的預設處理常式，則您的函式應傳回 S FALSE。 \_如果已處理訊息，則傳回 S OK。 否則，會傳回標準的 HRESULT 錯誤碼。

這則訊息會根據回呼的實作為方式傳送至回呼函式或回呼物件。 有兩個 Api 可用於回呼結構、 [**CDefFolderMenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2) ，其採用回呼函式的指標，或使用支援 [**ICoNtextMenuCB**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenucb)的回呼物件的 [**SHCreateDefaultCoNtextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu) 。

正在叫用命令的專案會在傳遞給回呼函式或 [**ICoNtextMenuCB：： callback**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenucb-callback) 方法的資料物件中提供。 這個資料物件是由執行回呼的資料來源所提供。 若要從資料物件中解壓縮專案，請使用 [**SHCreateShellItemArrayFromDataObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject)。

[**DFM \_INVOKECOMMAND**](dfm-invokecommand.md) 是此訊息較簡單的版本，不會提供太多的資訊給回呼。 如果您的執行不需要 **DFM \_ INVOKECOMMANDEX** 提供的額外資訊，請使用 **DFM \_ INVOKECOMMAND** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                      |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Shlobj.h。h</dt> </dl> |



 

 
