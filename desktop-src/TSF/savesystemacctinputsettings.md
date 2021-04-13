---
title: SaveSystemAcctInputSettings 函式
description: 將使用者鍵盤配置和文字服務設定套用至系統帳戶 hive。
ms.assetid: 73782637-3784-46d9-ba93-0527a2527412
keywords:
- SaveSystemAcctInputSettings 函式文字服務架構
topic_type:
- apiref
api_name:
- SaveSystemAcctInputSettings
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e45d590b80a9119d78eac8363a493ecd6c7b70d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104383970"
---
# <a name="savesystemacctinputsettings-function"></a>SaveSystemAcctInputSettings 函式

將使用者鍵盤配置和文字服務設定套用至系統帳戶 hive。

## <a name="syntax"></a>語法


```C++
BOOL CALLBACK SaveSystemAcctInputSettings(
  _In_ HWND hwndParent,
  _In_ HKEY hSourceRegKey
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hwndParent* \[在\]
</dt> <dd>

警告對話方塊的父視窗。 警告對話方塊不一定會顯示出來，而且會適當地出現。 如果此參數為 **Null**，則不會顯示警告對話方塊。

</dd> <dt>

*hSourceRegKey* \[在\]
</dt> <dd>

要複製之使用者設定的根登錄機碼。

</dd> </dl>

## <a name="return-value"></a>傳回值



| 傳回碼                                                                          | Description                               |
|--------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**真**</dt> </dl>  | 函數成功。<br/>   |
| <dl> <dt>**假**</dt> </dl> | 發生未指定的錯誤。<br/> |



 

## <a name="remarks"></a>備註

系統帳戶 hive 是 HKEY \_ USERS \\ 。預設值、HKEY \_ 使用者 \\ s-1-5-19，以及 HKEY \_ 使用者 \\ s-1-5-20。

## <a name="examples"></a>範例

沒有可定義此函式的匯入程式庫，因此必須使用 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)取得此函式的指標。 下列範例示範如何取得此函式的指標。

> [!Note]  
> 不當使用 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) 可能會載入錯誤的 DLL，進而危及應用程式的安全性。 請參閱 [動態連結程式庫搜尋順序](/windows/desktop/Dlls/dynamic-link-library-search-order) ，以取得如何使用不同版本的 Microsoft Windows 正確載入 dll 的相關資訊。

 


```C++
typedef HRESULT (WINAPI *PTF_ SAVESYSTEMACCTINPUTSETTINGS)(HWND hwndParent, HKEY hSourceRegKey);

HMODULE hInputDLL = LoadLibrary(TEXT("input.dll"));
BOOL bRet = FALSE;

if(hInputDLL == NULL)
{
    // Error loading module; fail as securely as possible. 
}
else
{
    PTF_ SAVESYSTEMACCTINPUTSETTINGS pfnSaveSystemAcctInputSettings;
    
    pfnSaveSystemAcctInputSettings = (PTF_ SAVESYSTEMACCTINPUTSETTINGS)GetProcAddress(hInputDLL, "SaveSystemAcctInputSettings ");

    if(pfnSaveSystemAcctInputSettings)
    {
        bRet = (*pfnSaveSystemAcctInputSettings)( hwndParent, hSourceRegKey);
    }

    FreeLibrary(hInputDLL);
}
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Input.dll</dt> </dl> |



 

