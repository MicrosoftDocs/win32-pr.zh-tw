---
description: 呼叫程式庫，以驗證是否可以安全地呼叫特定 CLSID。
ms.assetid: 94C8731B-88FD-4240-BF5D-2CD67C41B063
title: 'WldpIsClassInApprovedList 函式 (Wldp) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WldpIsClassInApprovedList
api_type:
- DllExport
api_location:
- wldp.dll
ms.openlocfilehash: 01762c60a3f1aef1574cc218ace9988669175efe
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110072"
---
# <a name="wldpisclassinapprovedlist-function"></a>WldpIsClassInApprovedList 函式

呼叫程式庫，以驗證是否可以安全地呼叫特定 **CLSID** 。 函數沒有相關聯的匯入程式庫。 您必須使用 LoadLibrary 和 GetProcAddress 函數，以動態方式連結至 wldp.dll。

## <a name="syntax"></a>語法


```C++
HRESULT WINAPI WldpIsClassInApprovedList(
        REFCLSID               classID,
  _In_  PWLDP_HOST_INFORMATION hostInformation,
  _Out_ PBOOL                  isApproved,
        DWORD                  optionalFlags
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*classID* 
</dt> <dd>

要檢查是否有核准的 COM 類別識別碼。

</dd> <dt>

*hostInformation* \[在\]
</dt> <dd>

識別要評估之主機的 [**WLDP \_ 主機 \_ 資訊**](wldp-host-information.md) 結構。

</dd> <dt>

*isApproved* \[擴展\]
</dt> <dd>

成功完成時，如果類別識別碼已核准，則會包含 **TRUE** 。否則 **為 FALSE**。

</dd> <dt>

*optionalFlags* 
</dt> <dd>

此參數是保留的，而且必須設定為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

**如果成功，則 \_ 此** 方法會傳回，否則會傳回失敗碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 10 桌面應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2016 \[ desktop 應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Wldp。h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Wldp.dll</dt> </dl> |



 

 




