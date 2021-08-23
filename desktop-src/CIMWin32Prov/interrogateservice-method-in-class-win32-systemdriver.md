---
description: 要求系統驅動程式服務將其狀態更新至 service manager。
ms.assetid: 350d9044-39fd-436f-ab15-b30324b2b2e9
ms.tgt_platform: multiple
title: Win32_SystemDriver 類別的 InterrogateService 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriver.InterrogateService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0327dc7dcb357217ff18df85b22c7cc7bff8972f42ebeb53a89f552c98205d72
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119760328"
---
# <a name="interrogateservice-method-of-the-win32_systemdriver-class"></a>Win32 >systemdriver 類別的 InterrogateService 方法 \_

**InterrogateService** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會要求系統驅動程式服務將其狀態更新為 service manager。

本主題使用受控物件格式 (MOF) 語法。 如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。

## <a name="syntax"></a>語法


```mof
uint32 InterrogateService();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

如果已接受 **InterrogateService** 要求，則傳回 0 (零) 的值，如果要求不受支援則為 1 (一個) ，以及表示錯誤的其他任何數位。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 命名空間<br/>                | 根 \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32 mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Win32 \_ >systemdriver**](win32-systemdriver.md)
</dt> <dt>

[作業系統類別](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**Win32 \_ BaseService**](win32-baseservice.md)
</dt> </dl>

 

