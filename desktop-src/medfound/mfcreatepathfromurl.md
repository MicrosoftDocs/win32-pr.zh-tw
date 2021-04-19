---
description: 將檔案 URL 轉換成 Microsoft MS-DOS 路徑。
ms.assetid: c35988ad-6cf8-41ec-bee9-e3bb982310ee
title: MFCreatePathFromURL 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MFCreatePathFromURL
api_type:
- DllExport
api_location:
- mfplat.dll
ms.openlocfilehash: c1838a3b09dc5375588d562aa503d555a186e394
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971454"
---
# <a name="mfcreatepathfromurl-function"></a>MFCreatePathFromURL 函式

\[此 API 不受支援，而且可能會在未來變更或無法使用。 相反地，應用程式應該呼叫 [**PathCreateFromUrl**](/windows/win32/api/shlwapi/nf-shlwapi-pathcreatefromurla)。\]

將檔案 URL 轉換成 Microsoft MS-DOS 路徑。

## <a name="syntax"></a>語法


```C++
HRESULT MFCreatePathFromURL(
  _In_opt_ LPCWSTR pwszFileURL,
  _Out_    LPWSTR  *ppwszFilePath
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pwszFileURL* \[在中，選擇性\]
</dt> <dd>

包含 URL 之以 null 終止的字串。 字串的最大長度為 **網際網路 \_ 最大 \_ URL \_ 長度**。

</dd> <dt>

*ppwszFilePath* \[擴展\]
</dt> <dd>

接收包含 URL 的以 null 終止的字串。 呼叫端必須藉由呼叫 [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree)來釋放字串。

</dd> </dl>

## <a name="return-value"></a>傳回值

函數會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                                  | Description                                                                                                 |
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>         | 此函數已成功。 <br/>                                                                         |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | 無效引數。 *PwszFileURL* 參數中提供的字串無法轉換成路徑。<br/> |



 

## <a name="remarks"></a>備註

此函數沒有相關聯的匯入程式庫。 若要呼叫這個函式，您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數，以動態方式連結至 Mfplat.dll。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Mfplat.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎函式](media-foundation-functions.md)
</dt> </dl>

 

 
