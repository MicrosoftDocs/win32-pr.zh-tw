---
description: SetSpeed 方法會要求風扇速度設定為在方法的輸入參數中指定的值。
ms.assetid: 7dd1cd57-66c5-4b50-9a73-31caf0b824e6
ms.tgt_platform: multiple
title: CIM_Fan 類別的 SetSpeed 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Fan.SetSpeed
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 16d90dbef3a9318ad144303e5720cea0abbde03e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847596"
---
# <a name="setspeed-method-of-the-cim_fan-class"></a>CIM 風扇類別的 SetSpeed 方法 \_

**SetSpeed** 方法會要求風扇速度設定為在方法的輸入參數中指定的值。

> [!IMPORTANT]
> DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。 WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。

 

本主題使用受控物件格式 (MOF) 語法。 如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。

## <a name="syntax"></a>語法


```mof
uint32 SetSpeed(
  [in] uint64 DesiredSpeed
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*DesiredSpeed* \[在\]
</dt> <dd>

要求的風扇速度，以每分鐘的旋轉。

</dd> </dl>

## <a name="return-value"></a>傳回值

在成功時傳回 0 (零) 的值; 如果不支援要求，則傳回 1 (一個) ，以及指定錯誤的任何其他數位。

## <a name="remarks"></a>備註

這個方法目前不是由 WMI 所執行。 若要使用這個方法，您必須在自己的提供者中加以執行。

此檔衍生自 DMTF 所發佈的 CIM 類別描述。 Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。

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

[CIM \_ 風扇](setspeed-method-in-class-cim-fan.md)
</dt> <dt>

[**CIM \_ 風扇**](cim-fan.md)
</dt> </dl>

 

