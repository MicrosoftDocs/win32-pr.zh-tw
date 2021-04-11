---
description: 將認證的輸出保護通訊協定 (COPP) 狀態要求傳送到受保護的輸出物件。
ms.assetid: 24300591-c0c0-48a2-99d3-be98c0c1492a
title: GetCOPPCompatibleOPMInformation 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCOPPCompatibleOPMInformation
api_type:
- DllExport
api_location:
- gdi32.dll
ms.openlocfilehash: 7e5eac24dfcf08e45ce414090835792e594d7c37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191052"
---
# <a name="getcoppcompatibleopminformation-function"></a>GetCOPPCompatibleOPMInformation 函式

> [!IMPORTANT]
> [輸出保護管理員](output-protection-manager.md)會使用此函式 (OPM) 來存取顯示驅動程式中的功能。 應用程式不應該呼叫此函式。

 

將認證的輸出保護通訊協定 (COPP) 狀態要求傳送到受保護的輸出物件。

## <a name="syntax"></a>語法


```C++
NTSTATUS WINAPI GetCOPPCompatibleOPMInformation(
  _In_  OPM_PROTECTED_OUTPUT_HANDLE                     opoOPMProtectedOutput,
  _In_  DXGKMDT_OPM_COPP_COMPATIBLE_GET_INFO_PARAMETERS *pParameters,
  _Out_ DXGKMDT_OPM_REQUESTED_INFORMATION               *pRequestedInformation
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*opoOPMProtectedOutput* \[在\]
</dt> <dd>

受保護之輸出物件的控制碼。 藉由呼叫 [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md)來取得此控制碼。

</dd> <dt>

*pParameters* \[在\]
</dt> <dd>

**DXGKMDT \_ OPM \_ COPP \_ 相容的 \_ GET \_ INFO \_ 參數** 結構的指標，其中包含狀態要求的輸入資料。

</dd> <dt>

*pRequestedInformation* \[擴展\]
</dt> <dd>

DXGKMDT OPM 的指標，其 **\_ 要求的 \_ \_ 資訊** 結構會接收狀態要求的結果。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果方法成功，則會傳回 **狀態 \_ 成功**。 否則，它會傳回一個 **NTSTATUS** 錯誤碼。

## <a name="remarks"></a>備註

應用程式應該呼叫 [**IOPMVideoOutput：： COPPCompatibleGetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation) ，而不是呼叫此函式。

您必須使用 COPP 語義來建立受保護的輸出物件。 請參閱 [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md)。

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

 

 
