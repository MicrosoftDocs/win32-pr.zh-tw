---
description: 啟動目前註冊此進程的偵錯工具。
ms.assetid: 63c30db8-6117-4353-9132-4f39c72a6637
ms.tgt_platform: multiple
title: Win32_Process 類別的 AttachDebugger 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Process.AttachDebugger
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 86ec5e31afef484733381d94bfdfa48595401d963443c2ab407ee6166d5d0f4b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118959167"
---
# <a name="attachdebugger-method-of-the-win32_process-class"></a>Win32 進程類別的 AttachDebugger 方法 \_

**AttachDebugger** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會啟動目前已針對此進程註冊的偵錯工具。

本主題使用受控物件格式 (MOF) 語法。 如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。

## <a name="syntax"></a>語法


```mof
uint32 AttachDebugger();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回下列清單所列的其中一個值，或任何其他值以表示錯誤。 如需其他錯誤代碼，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。 如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。

<dl> <dt>

**成功完成**
</dt> <dd>

0

順利完成。

</dd> <dt>

**拒絕存取**
</dt> <dd>

2

使用者無法存取所要求的資訊。

</dd> <dt>

**許可權不足**
</dt> <dd>

3

使用者沒有足夠的許可權。

</dd> <dt>

**未知的失敗**
</dt> <dd>

8

未知的失敗。

</dd> <dt>

**找不到路徑**
</dt> <dd>

9

指定的路徑不存在。

</dd> <dt>

**參數不正確**
</dt> <dd>

21

指定的參數無效。

</dd> <dt>

**其他**
</dt> <dd>

22 4294967295

</dd> </dl>

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

[作業系統類別](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**Win32 \_ 進程**](win32-process.md)
</dt> </dl>

 

