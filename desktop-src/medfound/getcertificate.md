---
description: 取得顯示驅動程式的憑證。
ms.assetid: eceaf151-1dae-4ff0-9139-7f1789f6c682
title: GetCertificate 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCertificate
api_type:
- DllExport
api_location:
- gdi32.dll
ms.openlocfilehash: 30cb17345177b552e51120afd00758a3f6886584
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973189"
---
# <a name="getcertificate-function"></a>GetCertificate 函式

> [!IMPORTANT]
> [輸出保護管理員](output-protection-manager.md)會使用此函式 (OPM) 來存取顯示驅動程式中的功能。 應用程式不應該呼叫此函式。

 

取得顯示驅動程式的憑證。

## <a name="syntax"></a>語法


```C++
NTSTATUS WINAPI GetCertificate(
  _In_  PUNICODE_STRING          pstrDeviceName,
  _In_  DXGKMDT_CERTIFICATE_TYPE ctPVPCertificateType,
  _Out_ BYTE                     *pbCertificate,
  _Out_ ULONG                    ulCertificateLength
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pstrDeviceName* \[在\]
</dt> <dd>

[**UNICODE \_ 字串**](/windows/win32/api/subauth/ns-subauth-unicode_string)結構的指標，其中包含 [**GetMonitorInfo**](/windows/win32/api/winuser/nf-winuser-getmonitorinfoa)函式所傳回之顯示裝置的名稱。

</dd> <dt>

*ctPVPCertificateType* \[在\]
</dt> <dd>

憑證的類型，指定為 **DXGKMDT \_ 憑證 \_ 類型** 列舉的成員。

</dd> <dt>

*pbCertificate* \[擴展\]
</dt> <dd>

接收憑證之緩衝區的指標。

</dd> <dt>

*ulCertificateLength* \[擴展\]
</dt> <dd>

*PbCertificate* 緩衝區的大小（以位元組為單位）。 若要取得憑證的大小，請呼叫 [**GetCertificateSize**](getcertificatesize.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果方法成功，則會傳回 **狀態 \_ 成功**。 否則，它會傳回一個 **NTSTATUS** 錯誤碼。

## <a name="remarks"></a>備註

應用程式應該呼叫 [**IOPMVideoOutput：： StartInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-startinitialization) 方法，而不是此函數。

此函數沒有相關聯的匯入程式庫。 若要呼叫這個函式，您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數，以動態方式連結至 Gdi32.dll。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Gdi32.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[OPM 函式](opm-functions.md)
</dt> <dt>

[輸出保護管理員](output-protection-manager.md)
</dt> </dl>

 

 
