---
description: 在受保護的輸出物件上設定簽署金鑰和兩個序號。
ms.assetid: 278a80f5-198d-4311-aa43-10b6dc33b3a4
title: SetOPMSigningKeyAndSequenceNumbers 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetOPMSigningKeyAndSequenceNumbers
api_type:
- DllExport
api_location:
- gdi32.dll
ms.openlocfilehash: 7096b45d722ecbd3d70048a3e6de8cd6de260741abdb610f52a0694ca5ee6200
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119953208"
---
# <a name="setopmsigningkeyandsequencenumbers-function"></a>SetOPMSigningKeyAndSequenceNumbers 函式

> [!IMPORTANT]
> [輸出保護管理員](output-protection-manager.md)會使用此函式 (OPM) 來存取顯示驅動程式中的功能。 應用程式不應該呼叫此函式。

 

在受保護的輸出物件上設定簽署金鑰和兩個序號。

## <a name="syntax"></a>語法


```C++
NTSTATUS WINAPI SetOPMSigningKeyAndSequenceNumbers(
  _In_        OPM_PROTECTED_OUTPUT_HANDLE      opoOPMProtectedOutput,
  _Out_ const DXGKMDT_OPM_ENCRYPTED_PARAMETERS *pParameters
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*opoOPMProtectedOutput* \[在\]
</dt> <dd>

受保護之輸出物件的控制碼。 藉由呼叫 [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md)來取得此控制碼。

</dd> <dt>

*pParameters* \[擴展\]
</dt> <dd>

包含256位元組陣列的 [**DXGKMDT \_ OPM \_ 加密 \_ 參數**](/windows-hardware/drivers/ddi/d3dkmdt/ns-d3dkmdt-_dxgkmdt_opm_encrypted_parameters) 結構指標。 如需如何初始化此陣列的詳細資訊，請參閱 [DxgkDdiOPMSetSigningKeyAndSequenceNumbers](https://msdn.microsoft.com/library/aa906703.aspx)。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果方法成功，則會傳回 **狀態 \_ 成功**。 否則，它會傳回一個 **NTSTATUS** 錯誤碼。

## <a name="remarks"></a>備註

應用程式應該呼叫 [**IOPMVideoOutput：： FinishInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-finishinitialization) ，而不是呼叫此函式。

此函數沒有相關聯的匯入程式庫。 若要呼叫這個函式，您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數，以動態方式連結至 Gdi32.dll。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Gdi32.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[OPM 函式](opm-functions.md)
</dt> <dt>

[輸出保護管理員](output-protection-manager.md)
</dt> </dl>

 

 
