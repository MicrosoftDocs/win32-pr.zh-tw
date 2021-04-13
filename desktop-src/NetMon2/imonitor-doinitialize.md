---
description: DoInitialize 方法必須由監視器所執行。 在呼叫 NPPs IRTCConnect 方法之前，MCSVC 會呼叫這個方法來立即取得 capture 篩選器。
ms.assetid: 5e43be75-21b3-4f37-ad53-3ffdd55f56a1
title: 'IMonitorDoInitialize 方法 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitor.DoInitialize
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: 93133ce8204e49d080f87635ad6952685f2ba82d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510967"
---
# <a name="imonitordoinitialize-method"></a>IMonitor：:D oInitialize 方法

**DoInitialize** 方法必須由監視器所執行。 在呼叫 NPP 的 [IRTC：： Connect](irtc-connect.md) 方法之前，MCSVC 會呼叫這個方法來立即取得 capture 篩選器。

## <a name="syntax"></a>語法


```C++
HRESULT DoInitialize(
  [in]      IUnknown *pUnkMonitorCtrl,
  [in, out] HBLOB    hNPPBlob
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pUnkMonitorCtrl* \[在\]
</dt> <dd>

MCSVC 傳入的 [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) 指標。 若要取得支援的監視器控制項介面，監視器必須在指標上呼叫 [IUnknown：： QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) 。

</dd> <dt>

*hNPPBlob* \[in、out\]
</dt> <dd>

在輸入上，NPP BLOB 的控制碼。

在輸出中，包含 capture 篩選的 NPP BLOB。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果方法成功，則傳回值為 S \_ OK (與 >aad-userreadusingalternativesecurityid-noerror) 相同。

如果此方法不成功，則傳回值會是錯誤碼。 發生錯誤時，MCSVC 不會在介面指標上建立監視或呼叫 [IUnknown：： Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) 。

## <a name="remarks"></a>備註

MCSVC 會呼叫 **DoInitialize** 方法，以執行任何必要的監視器初始化。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl> |



 

