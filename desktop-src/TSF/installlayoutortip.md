---
title: InstallLayoutOrTip 函式
description: 啟用指定的鍵盤配置或文字服務。
ms.assetid: 6542ad85-02fb-4a57-b665-ff367ba4e99c
keywords:
- InstallLayoutOrTip 函式文字服務架構
topic_type:
- apiref
api_name:
- InstallLayoutOrTip
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7fd3825903f4c92de93709385b03f9e9cba5db84
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966314"
---
# <a name="installlayoutortip-function"></a>InstallLayoutOrTip 函式

啟用指定的鍵盤配置或文字服務。

## <a name="syntax"></a>語法


```C++
BOOL CALLBACK InstallLayoutOrTip(
  _In_ LPCWSTR psz,
  _In_ DWORD   dwFlags
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

指定下列旗標的位位：

> [!Note]  
> 下列識別碼未在公用標頭檔中定義。 您必須使用十六進位值或 \# 定義識別碼。 例如，若要使用 **ILOT \_ 卸載** ，您必須 `#define ILOT_UNINSTALL 0x00000001` 將程式碼包含在程式碼中。

 



| 值                                                                                                                                                                                                                                                                      | 意義                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <span id="ILOT_UNINSTALL"></span><span id="ilot_uninstall"></span><dl> <dt>**ILOT \_卸載**</dt> <dt>0x00000001</dt> </dl>                                           | 與 **ILOT \_ 已停用**。<br/>                                     |
| <span id="ILOT_DEFPROFILE"></span><span id="ilot_defprofile"></span><dl> <dt>**ILOT \_DEFPROFILE**</dt> <dt>0x00000002</dt> </dl>                                        | 將指定的版面配置或提示設定為預設專案。<br/>             |
| <span id="ILOT_DEFUSER4"></span><span id="ilot_defuser4"></span><dl> <dt>**ILOT \_DEFUSER4**</dt> <dt>0x00000004</dt> </dl>                                              | 變更的設定。預設。<br/>                                |
| <span id="ILOT_SYSLOCALE"></span><span id="ilot_syslocale"></span><dl> <dt>**ILOT \_SYSLOCALE**</dt> <dt>0x00000008</dt> </dl>                                           | 未使用的。<br/>                                                         |
| <span id="ILOT_NOLOCALETOENUMERATE"></span><span id="ilot_nolocaletoenumerate"></span><dl> <dt>**ILOT \_NOLOCALETOENUMERATE**</dt> <dt>0x00000010</dt> </dl>             | 未使用的。<br/>                                                         |
| <span id="ILOT_NOAPPLYTOCURRENTSESSION"></span><span id="ilot_noapplytocurrentsession"></span><dl> <dt>**ILOT \_NOAPPLYTOCURRENTSESSION**</dt> <dt>0x00000020</dt> </dl> | 這項設定會儲存，但不會套用到目前的會話。<br/> |
| <span id="ILOT_CLEANINSTALL"></span><span id="ilot_cleaninstall"></span><dl> <dt>**ILOT \_CLEANINSTALL**</dt> <dt>0x00000040</dt> </dl>                                  | 停用所有目前的鍵盤配置和文字服務。<br/> |
| <span id="ILOT_DISABLED"></span><span id="ilot_disabled"></span><dl> <dt>**ILOT \_停用**</dt>的 <dt>0x00000080</dt> </dl>                                              | 停用指定的鍵盤配置和文字服務。<br/>        |



 

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

沒有可定義此函式的匯入程式庫，因此必須使用 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)取得此函式的指標。

> [!Note]  
> 不當使用 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) 可能會載入錯誤的 DLL，進而危及應用程式的安全性。 請參閱 [動態連結程式庫搜尋順序](/windows/desktop/Dlls/dynamic-link-library-search-order) ，以取得如何使用不同版本的 Microsoft Windows 正確載入 dll 的相關資訊。

 


```C++
typedef HRESULT (WINAPI *PTF_ INSTALLLAYOUTORTIP)(LPCWSTR psz, DWORD dwFlasg);

HMODULE hInputDLL = LoadLibrary(TEXT("input.dll"));
BOOL bRet = FALSE;

if(hInputDLL == NULL)
{
    // Error loading module; fail as securely as possible. 
}
else
{
    PTF_ INSTALLLAYOUTORTIP pfnInstallLayoutOrTip;
    
    pfnInstallLayoutOrTip = (PTF_ INSTALLLAYOUTORTIP)GetProcAddress(hInputDLL, "InstallLayoutOrTip");

    if(pfnInstallLayoutOrTip)
    {
        bRet = (*pfnInstallLayoutOrTip)(psz, dwFlags);
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



 

