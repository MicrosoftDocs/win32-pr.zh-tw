---
description: 將 Microsoft MS-DOS 路徑轉換成正式的 URL。
ms.assetid: 1186b970-9ae1-4020-b999-55157cff1741
title: MFCreateURLFromPath 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MFCreateURLFromPath
api_type:
- DllExport
api_location:
- mfplat.dll
ms.openlocfilehash: e43c2d7df299792d8b5be99226e9cfdbd11976a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106966765"
---
# <a name="mfcreateurlfrompath-function"></a>MFCreateURLFromPath 函式

\[此 API 不受支援，而且可能會在未來變更或無法使用。 相反地，應用程式應該呼叫 [UrlCreateFromPath](/windows/desktop/api/shlwapi/nf-shlwapi-urlcreatefrompatha)。\]

將 Microsoft MS-DOS 路徑轉換成正式的 URL。

## <a name="syntax"></a>語法


```C++
HRESULT MFCreateURLFromPath(
  _In_opt_ LPCWSTR pwszFilePath,
  _Out_    LPWSTR  *ppwszFileURL
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pwszFilePath* \[在中，選擇性\]
</dt> <dd>

包含路徑之以 null 終止的字串。 字串的最大長度為 **網際網路 \_ 最大 \_ URL \_ 長度**。

</dd> <dt>

*ppwszFileURL* \[擴展\]
</dt> <dd>

接收包含 URL 的以 null 終止的字串。 呼叫端必須藉由呼叫 [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree)來釋放字串。

</dd> </dl>

## <a name="return-value"></a>傳回值

函數會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                             | Description                                                                                                                                                               |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl> | *PwszFilePath* 參數中提供的字串已經是 URL 格式。 在此情況下， *pszFilePath* 只會複製到 *ppszFileURL* 而不需要修改。<br/> |
| <dl> <dt>**S \_ 確定**</dt> </dl>    | 此函數已成功。 <br/>                                                                                                                                       |



 

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

 

 
