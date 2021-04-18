---
title: EnumEnabledLayoutOrTip 函式
description: 列舉所指定使用者設定的所有已啟用鍵盤配置或文字服務。
ms.assetid: b3c57e88-e04b-411b-9eba-83258da16773
keywords:
- EnumEnabledLayoutOrTip 函式文字服務架構
topic_type:
- apiref
api_name:
- EnumEnabledLayoutOrTip
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b192896dd95d5ab8f306158e33a8d248793bfc10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968962"
---
# <a name="enumenabledlayoutortip-function"></a>EnumEnabledLayoutOrTip 函式

列舉所指定使用者設定的所有已啟用鍵盤配置或文字服務。

## <a name="syntax"></a>語法


```C++
UINT EnumEnabledLayoutOrTip(
  _In_opt_ LPCWSTR            pszUserReg,
  _In_opt_ LPCWSTR            pszSystemReg,
  _In_opt_ LPCWSTR            pszSoftwareReg,
  _Out_    LAYOUTORTIPPROFILE *pLayoutOrTipProfile,
  _In_     UINT               uBufLength
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pszUserReg* \[在中，選擇性\]
</dt> <dd>

使用者的登錄路徑。 如果此參數為 **Null**， \_ \_ 則會使用 HKEY 目前的使用者。

</dd> <dt>

*pszSystemReg* \[在中，選擇性\]
</dt> <dd>

系統的登錄路徑。 如果此參數為 **Null**， \_ \_ \\ 則會使用 HKEY 本機電腦系統。

</dd> <dt>

*pszSoftwareReg* \[在中，選擇性\]
</dt> <dd>

軟體的登錄路徑。 如果此參數為 **Null**， \_ \_ \\ 則會使用 HKEY 本機電腦軟體。

</dd> <dt>

*pLayoutOrTipProfile* \[擴展\]
</dt> <dd>

接收 LAYOUTORTIPPROFILE 陣列的緩衝區指標。

</dd> <dt>

*uBufLength* \[在\]
</dt> <dd>

*PLayoutOrTipProfile* 所指向的緩衝區長度。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果 *pLayoutOrTipProfile* 為 **Null**，則為使用者設定中啟用的鍵盤專案數目;否則，會複製到 *pLayoutOrTipProfile* 中的鍵盤專案數目。

針對輸入法 (IME) 語言，即使只有一個 IME 啟用，也會傳回所有的 ime。 例如，如果使用者已啟用 CHT New Quick IME， **EnumEnabledLayoutOrTip** 函式會傳回所有5個 CHT 的 ime。

## <a name="remarks"></a>備註

沒有可定義此函式的匯入程式庫，因此必須使用 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)取得此函式的指標。

> [!Note]  
> 不當使用 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) 可能會載入錯誤的 DLL，進而危及應用程式的安全性。 請參閱 [動態連結程式庫搜尋順序](/windows/desktop/Dlls/dynamic-link-library-search-order) ，以取得如何使用不同版本的 Microsoft Windows 正確載入 dll 的相關資訊。

 

LAYOUTORTIPPROFILE 的定義如下：

``` syntax
typedef struct tagLAYOUTORTIPPROFILE {
    DWORD  dwProfileType;       // InputProcessor or HKL 
#define LOTP_INPUTPROCESSOR 1
#define LOTP_KEYBOARDLAYOUT 2
    LANGID langid;              // language id 
    CLSID  clsid;               // CLSID of tip 
    GUID   guidProfile;         // profile description 
    GUID   catid;               // category of tip 
    DWORD  dwSubstituteLayout;  // substitute hkl 
    DWORD  dwFlags;             // Flags 
    WCHAR  szId[MAX_PATH];      // KLID or TIP profile for string 
} LAYOUTORTIPPROFILE;
```

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Input.dll</dt> </dl> |



 

