---
title: 'MPCLEAN_PRECHECK_DATA 結構 (MpClient .h) '
description: 傳遞給清除前置檢查回呼函數的通知資料。
ms.assetid: 65B3B116-6E83-46F5-AE2B-92A41AE39480
keywords:
- MPCLEAN_PRECHECK_DATA 結構舊版 Windows 環境功能
- PMPCLEAN_PRECHECK_DATA 結構指標舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MPCLEAN_PRECHECK_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc272ed230a67811497f0eebb99624d74369c8c55419fba970f326fba502e8b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118747924"
---
# <a name="mpclean_precheck_data-structure"></a>MPCLEAN \_ 檢查 \_ 資料結構

傳遞給清除前置檢查回呼函數的通知資料。

## <a name="syntax"></a>語法


```C++
typedef struct tagMPCLEAN_PRECHECK_DATA {
  PMPRESOURCE_INFO     BlockedResourceInfo;
  BlockingResourceInfo PMPRESOURCE_INFO;
} MPCLEAN_PRECHECK_DATA, *PMPCLEAN_PRECHECK_DATA;
```



## <a name="members"></a>成員

<dl> <dt>

**BlockedResourceInfo**
</dt> <dd>

類型： **PMPRESOURCE \_ 資訊**

</dd> <dd>

有關被封鎖之資源的資源資訊。 例如，當進度是封鎖 MPNOTIFY 的前置檢查 **\_ \_ 資源 \_** 時。 請參閱 [**MPRESOURCE \_ 資訊**](mpresource-info.md)。

</dd> <dt>

**PMPRESOURCE \_ 資訊**
</dt> <dd>

類型： **BlockingResourceInfo**

</dd> <dd>

有關封鎖之資源的資源資訊。 例如，當進度是封鎖 MPNOTIFY 的前置檢查 **\_ \_ 資源 \_** 時。 請參閱 [**MPRESOURCE \_ 資訊**](mpresource-info.md)。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>MpClient。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MPRESOURCE \_ 資訊**](mpresource-info.md)
</dt> </dl>

 

 





