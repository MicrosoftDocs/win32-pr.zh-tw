---
description: 建立 capture 引擎的實例。
ms.assetid: 4B0C9DD6-135D-4412-A585-7E98A84101B5
title: MFCreateCaptureEngine 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MFCreateCaptureEngine
api_type:
- DllExport
api_location:
- MFCaptureEngine.dll
ms.openlocfilehash: 18d264b30b8f3ed4d06e80f236908dd7bc81dbe96c4eb9c3231fa330331e34f5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119940248"
---
# <a name="mfcreatecaptureengine-function"></a>MFCreateCaptureEngine 函式

\[MFCreateCaptureEngine 不受支援，未來可能會變更或無法使用。 \]

建立 capture 引擎的實例。

## <a name="syntax"></a>語法


```C++
HRESULT MFCreateCaptureEngine(
  _Out_ IMFCaptureEngine **ppCaptureEngine
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppCaptureEngine* \[擴展\]
</dt> <dd>

接收 [**IMFCaptureEngine**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcaptureengine) 介面的指標。 呼叫端必須釋放介面。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則會傳回 S \_ OK。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

此函式沒有相關聯的匯入程式庫，且未在公用標頭檔中宣告。 您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數，以動態方式連結至 MFCaptureEngine.dll。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                                     |
| 最低支援的伺服器<br/> | Windows Server 2012\[僅限 R2 desktop 應用程式\]<br/>                                        |
| DLL<br/>                      | <dl> <dt>MFCaptureEngine.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎函式](media-foundation-functions.md)
</dt> </dl>

 

 
