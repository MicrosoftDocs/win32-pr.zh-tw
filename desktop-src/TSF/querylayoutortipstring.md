---
title: QueryLayoutOrTipString 函式
description: 查詢指定的字串，表示鍵盤配置清單或文字服務配置檔案清單的格式。
ms.assetid: 92fd89b7-8b96-4709-8ee2-9814a908b4e4
keywords:
- QueryLayoutOrTipString 函式文字服務架構
topic_type:
- apiref
api_name:
- QueryLayoutOrTipString
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11f4cead682a50897a74c60eeadf886e8b47456b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106983316"
---
# <a name="querylayoutortipstring-function"></a>QueryLayoutOrTipString 函式

查詢指定的字串，表示鍵盤配置清單或文字服務配置檔案清單的格式。

## <a name="syntax"></a>語法


```C++
HRESULT CALLBACK QueryLayoutOrTipString(
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

這必須是 0。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函數可以傳回其中一個值。



| 傳回碼                                                                                  | Description                                                                     |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>         | *Psz* 中定義的所有版面配置或設定檔都有效。<br/>                  |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | *Psz* 中定義的一或多個版面配置或設定檔無效。<br/> |



 

## <a name="remarks"></a>備註

沒有可定義此函式的匯入程式庫，因此必須使用 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)取得此函式的指標。

> [!Note]  
> 不當使用 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) 可能會載入錯誤的 DLL，進而危及應用程式的安全性。 請參閱 [動態連結程式庫搜尋順序](/windows/desktop/Dlls/dynamic-link-library-search-order) ，以取得如何使用不同版本的 Microsoft Windows 正確載入 dll 的相關資訊。

 

版面配置清單的字串格式為：

<LangID 1>： <KLID 1>; \[...<LangID N>:<KLID N>

文字服務配置檔案清單的字串格式為：

&lt;LangID 1&gt;： {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx} {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx} {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}; < a0/

以下是 *psz* 參數值的範例：

``` syntax
"0x0407:0x00000407"
"0x0407:0x00000407;0x040C:0x0000040C"
"0x0407:0x00000407;0x0412:{A028AE76-01B1-46C2-99C4-ACD9858AE02F}{B5FE1F02-D5F2-4445-9C03-C568F23C99A1};0x040C:0x0000040C"
```

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Input.dll</dt> </dl> |



 

