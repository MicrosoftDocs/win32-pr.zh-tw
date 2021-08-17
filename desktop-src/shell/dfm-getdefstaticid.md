---
description: 在建立期間由預設的內容功能表執行所傳送，指定預設的功能表命令，並允許進行替代選擇。 由 LPFNDFMCALLBACK 使用。
title: 'DFM_GETDEFSTATICID 訊息 (Shlobj.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 9e4ad96e-7c90-456e-8668-21b347f2915c
api_name:
- DFM_GETDEFSTATICID
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 4d987e085779fd58f16c2534b517c39ebb4b7e3c6e2829982881015bb3a59a92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119094369"
---
# <a name="dfm_getdefstaticid-message"></a>DFM \_ GETDEFSTATICID 訊息

在建立期間由預設的內容功能表執行所傳送，指定預設的功能表命令，並允許進行替代選擇。 由 [**LPFNDFMCALLBACK**](/windows/win32/api/shlobj_core/nc-shlobj_core-lpfndfmcallback)使用。


```C++
DFM_GETDEFSTATICID
    lParam = (LPARAM)(int*) defaultID;          
            
```



## <a name="parameters"></a>參數

<dl> <dt>

*defaultID* \[in、out\]
</dt> <dd>

所選功能表命令的識別碼指標。 可辨識下列旗標。

<dt>

<span id="DFM_CMD_PROPERTIES"></span><span id="dfm_cmd_properties"></span>

<span id="DFM_CMD_PROPERTIES"></span><span id="dfm_cmd_properties"></span>**DFM \_ CMD \_ 屬性**


</dt> <dd>

顯示在其上叫用功能表之專案的 [ **屬性** ] UI。

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>備註

若要覆寫預設的命令選擇，您的處理常式應該在收到此訊息時，將 *defaultID* 所指向的值設定為取代命令的識別碼，並傳回 \_ [確定]。 傳回失敗碼，否則為。

這則訊息會根據預設內容功能表物件的建立方式，傳送至回呼函式或回呼物件。 有兩個 Api 適用于其結構： [**CDefFolderMenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2)、 [**SHCreateDefaultCoNtextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu)。

[**DFM \_INVOKECOMMANDEX**](dfm-invokecommandex.md) 是此訊息的擴充版本，可提供更多的回呼資訊。 如果您的實作需要該介面所提供的其他資訊，請使用 **DFM \_ INVOKECOMMANDEX** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Shlobj.h。h</dt> </dl> |



 

 
