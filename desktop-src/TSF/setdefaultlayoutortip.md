---
title: SetDefaultLayoutOrTip 函式
description: 將指定的鍵盤配置或文字服務設定為目前使用者的預設輸入專案。
ms.assetid: e602065c-776b-47ba-b050-4325197e03de
keywords:
- SetDefaultLayoutOrTip 函式文字服務架構
topic_type:
- apiref
api_name:
- SetDefaultLayoutOrTip
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbdb2f2174c4a6d5ec37d5880d4a8b6feef236be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094143"
---
# <a name="setdefaultlayoutortip-function"></a>SetDefaultLayoutOrTip 函式

將指定的鍵盤配置或文字服務設定為目前使用者的預設輸入專案。

## <a name="syntax"></a>語法


```C++
BOOL CALLBACK SetDefaultLayoutOrTip(
  _In_ LPCWSTR           psz,
  _In_ LPCWSTR psz DWORD dwFlags
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*psz* \[在\]
</dt> <dd>

表示鍵盤配置清單或文字服務配置檔案清單的字串。

</dd> <dt>

*dwFlags* \[在\]
</dt> <dd>

指定下列旗標的位位。

> [!Note]  
> 下列識別碼未在公用標頭檔中定義。 您必須使用十六進位值或 \# 定義識別碼。 例如，若要使用 SDLOT \_ NOAPPLYTOCURRENTSESSION，您必須 \# \_ 在程式碼中包含定義 SDLOT NOAPPLYTOCURRENTSESSION 0x00000001。

 



| 值                                                                                                                                                                                                                                                                         | 意義                                                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SDLOT_NOAPPLYTOCURRENTSESSION"></span><span id="sdlot_noapplytocurrentsession"></span><dl> <dt>**SDLOT \_NOAPPLYTOCURRENTSESSION**</dt> <dt>0x00000001</dt> </dl> | 將設定儲存在登錄中，但無法更新目前會話的執行時間鍵盤設定。 如果在 [**SetDefaultLayoutOrTipUserReg**](/windows/desktop/TSF/setdefaultlayoutortipuserreg)中設定了替代登錄路徑，則應該設定此旗標。<br/> |
| <span id="SDLOT_APPLYTOCURRENTTHREAD"></span><span id="sdlot_applytocurrentthread"></span><dl> <dt>**SDLOT \_APPLYTOCURRENTTHREAD**</dt> <dt>0x00000002</dt> </dl>          | 立即在目前的執行緒上套用設定。<br/>                                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a>傳回值



| 傳回碼                                                                          | Description                               |
|--------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**真**</dt> </dl>  | 函數成功。<br/>   |
| <dl> <dt>**假**</dt> </dl> | 發生未指定的錯誤。<br/> |



 

## <a name="remarks"></a>備註

版面配置清單的字串格式為：

<LangID 1>： <KLID 1>; \[...<LangID N>:<KLID N>

文字服務配置檔案清單的字串格式為：

&lt;LangID 1&gt;： {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx} {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx} {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}; < a0/

以下是 *psz* 參數值的範例：


```C++
"0x0407:0x00000407"
"0x0407:0x00000407;0x040C:0x0000040C"
"0x0407:0x00000407;0x0412:{A028AE76-01B1-46C2-99C4-ACD9858AE02F}{B5FE1F02-D5F2-4445-9C03-C568F23C99A1};0x040C:0x0000040C"
```



## <a name="examples"></a>範例

沒有可定義此函式的匯入程式庫，因此必須使用 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)取得此函式的指標。 下列範例示範如何取得此函式的指標。

> [!Note]  
> 不當使用 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) 可能會載入錯誤的 DLL，進而危及應用程式的安全性。 請參閱 [動態連結程式庫搜尋順序](/windows/desktop/Dlls/dynamic-link-library-search-order) ，以取得如何使用不同版本的 Microsoft Windows 正確載入 dll 的相關資訊。

 


```C++
typedef HRESULT (WINAPI *PTF_ SETDEFAULTLAYOUTORTIP)(LPCWSTR psz);

HMODULE hInputDLL = LoadLibrary(TEXT("input.dll"));
BOOL bRet = FALSE;

if(hInputDLL == NULL)
{
    // Error loading module; fail as securely as possible. 
}
else
{
    PTF_ SETDEFAULTLAYOUTORTIP pfnSetDefaultLayoutOrTip;
    
    pfnSetDefaultLayoutOrTip = (PTF_ SETDEFAULTLAYOUTORTIP)GetProcAddress(hInputDLL, "SetDefaultLayoutOrTip");

    if(pfnSetDefaultLayoutOrTip)
    {
        bRet = (*pfnSetDefaultLayoutOrTip)(psz);
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



 

