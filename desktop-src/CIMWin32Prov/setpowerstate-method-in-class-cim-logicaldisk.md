---
description: CIM LogicalDisk 類別的 SetPowerState 方法 \_ 會設定邏輯裝置所需的電源狀態，以及何時應將裝置置於該狀態。
ms.assetid: bb363434-2fb5-422e-aea7-5c7de1364b88
ms.tgt_platform: multiple
title: CIM_LogicalDisk 類別的 SetPowerState 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDisk.SetPowerState
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: f97649a00f5e00e9fa098baeb2e6056080f41401
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111408"
---
# <a name="setpowerstate-method-of-the-cim_logicaldisk-class"></a>CIM LogicalDisk 類別的 SetPowerState 方法 \_

CIM LogicalDisk 類別的 **SetPowerState** 方法 \_ 會設定邏輯裝置所需的電源狀態，以及何時應將裝置置於該狀態。 在子類別中，您應該使用方法上的 **ValueMap** 辨識符號來指定可能的傳回碼集。 您也應該在子類別中，以 **值** 陣列限定詞的形式指定要轉譯之 **ValueMap** 內容的字串。 這個方法繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。

> [!IMPORTANT]
> DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。 WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。

 

## <a name="syntax"></a>語法


```mof
uint32 SetPowerState(
  [in] uint16   PowerState,
  [in] datetime Time
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*>powerstate* \[在\]
</dt> <dd>

指定此邏輯裝置所需電源狀態的 **ValueMap** 值。

<dt>

1
</dt> <dd>

完整功能。

</dd> <dt>

2
</dt> <dd>

省電低電源模式。

</dd> <dt>

3
</dt> <dd>

省電待命。

</dd> <dt>

4
</dt> <dd>

省電。

</dd> <dt>

5
</dt> <dd>

電源週期。

</dd> <dt>

6
</dt> <dd>

關閉電源。

</dd> </dl> </dd> <dt>

*時間* \[在\]
</dt> <dd>

指定何時應設定電源狀態，以做為一般日期時間值或做為間隔值， (在) 收到方法調用時的間隔開始時間。 當 *>powerstate* 參數等於 5 ( 「電源週期」 ) 時，時間參數會指出裝置應該重新開啟電源的 *時間* 。 立即關閉電源。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回 0 (零) 1 (一個) 如果不支援指定的 *>powerstate* 和 *時間* 要求，則傳回另一個值，如果發生任何其他錯誤，則傳回另一個值。

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

[CIM \_ LogicalDisk](setpowerstate-method-in-class-cim-logicaldisk.md)
</dt> <dt>

[**CIM \_ LogicalDisk**](cim-logicaldisk.md)
</dt> </dl>

 

 




