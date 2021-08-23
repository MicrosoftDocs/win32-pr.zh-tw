---
description: GetDescriptor 方法會傳回輸入參數所指定的 USB 中樞描述元。
ms.assetid: 0090da35-0de1-4ea5-b983-bd9bf9997009
ms.tgt_platform: multiple
title: 'CIM_USBHub 類別的 GetDescriptor 方法 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_USBHub.GetDescriptor
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5253f0eae0acf8844e844f5bfb48fcd73b2b186c6537dfcfcb0da5fb8f46582f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119879048"
---
# <a name="getdescriptor-method-of-the-cim_usbhub-class"></a>CIM USBHub 類別的 GetDescriptor 方法 \_

**GetDescriptor** 方法會傳回輸入參數所指定的 USB 中樞描述元。

> [!IMPORTANT]
> DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。 WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。

 

本主題使用受控物件格式 (MOF) 語法。 如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。

## <a name="syntax"></a>語法


```mof
uint32 GetDescriptor(
  [in]      uint8  RequestType,
  [in]      uint16 RequestValue,
  [in]      uint16 RequestIndex,
  [in, out] uint16 RequestLength,
  [out]     uint8  Buffer[]
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*RequestType* \[在\]
</dt> <dd>

描述項要求類型和收件者的位對應識別碼。 如需每個位的適當值，請參閱 USB 規格。

</dd> <dt>

*RequestValue* \[在\]
</dt> <dd>

包含在高位元組和描述元索引中的描述元類型 (例如，在低位元組中的描述元陣列) 的索引或位移。 如需詳細資訊，請參閱 USB 規格。

</dd> <dt>

*RequestIndex* \[在\]
</dt> <dd>

指定傳回字串描述中繼資料時，USB 裝置所使用的2位元組語言識別項程式碼。 參數通常是非字串描述項的 0 (零) 。 如需詳細資訊，請參閱 USB 規格。

</dd> <dt>

*RequestLength* \[in、out\]
</dt> <dd>

在輸入時，長度會 (為應傳回之描述項的八位) 。 如果這個值小於描述項的實際長度，則只會傳回要求的長度。 如果超過實際的長度，則會傳回實際長度。

在輸出時，長度會在傳回的緩衝區中，以八位)  (。 如果要求的描述項不存在，則此參數的內容為未定義。

</dd> <dt>

*緩衝區* \[擴展\]
</dt> <dd>

Buffer 會傳回要求的描述項資訊。 如果描述項不存在，則會未定義緩衝區的內容。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功傳回 USB 描述項，則傳回 0 (零) 的值，如果要求不受支援則為 1 (一個) ，以及表示錯誤的其他任何數位。 在子類別中，可能會使用方法上的 **ValueMap** 辨識符號來指定可能的傳回碼集。 要轉譯 **mofqualifier** 內容的字串，也可以在子類別中指定為 **值** 陣列限定詞。

## <a name="remarks"></a>備註

這個方法目前不是由 WMI 所執行。 若要使用這個方法，您必須在自己的提供者中加以執行。

此檔衍生自 DMTF 所發佈的 CIM 類別描述。 Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 命名空間<br/>                | 根 \\ CIMV2<br/>                                                                  |
| 標頭<br/>                   | <dl> <dt>Wmcodecdsp。h</dt> </dl> |
| MOF<br/>                      | <dl> <dt>CIMWin32 mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CIM \_ USBHub**](getdescriptor-method-in-class-cim-usbhub.md)
</dt> <dt>

[**CIM \_ USBHub**](cim-usbhub.md)
</dt> </dl>

 

