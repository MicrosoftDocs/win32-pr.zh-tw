---
description: 傳回輸入參數所指定的 USBDevice 描述元。
ms.assetid: 89bb8a49-6fca-422c-808d-70ae77aae4c3
title: 'CIM_USBDevice 類別的 GetDescriptor 方法 (Hyper-v 管理) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_USBDevice.GetDescriptor
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: f6aa8e7dc37f2bb7fe48ce0293bbaad9663150dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977857"
---
# <a name="getdescriptor-method-of-the-cim_usbdevice-class-hyper-v-management"></a>CIM_USBDevice 類別的 GetDescriptor 方法 (Hyper-v 管理) 

傳回輸入參數所指定的 USBDevice 描述元。

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

識別描述項要求類型和收件者的位對應。 要求的類型可能是「標準」、「類別」或「供應商特定」。 收件者可以是「裝置」、「介面」、「端點」或「其他」。 請參閱 USB 規格，以取得每個位的適當值。

</dd> <dt>

*RequestValue* \[在\]
</dt> <dd>

包含在高位元組和描述元索引中的描述元類型 (例如，在低位元組中的描述元陣列) 的索引或位移。 如需詳細資訊，請參閱 USB 規格。

</dd> <dt>

*RequestIndex* \[在\]
</dt> <dd>

定義傳回字串描述中繼資料時，USBDevice 所使用的2位元組語言識別項程式碼。 非字串描述項的參數通常是0。 如需詳細資訊，請參閱 USB 規格。

</dd> <dt>

*RequestLength* \[in、out\]
</dt> <dd>

在輸入上，包含應傳回之描述項的長度 (以八位) 。 如果這個值小於描述項的實際長度，則只會傳回要求的長度。 如果超過實際的長度，則會傳回實際長度。 在輸出中，這個參數是要傳回之緩衝區的長度（以八位）。 如果要求的描述項不存在，則此參數的內容為未定義。

</dd> <dt>

*緩衝區* \[擴展\]
</dt> <dd>

傳回要求的描述項資訊。 如果描述項不存在，則參數的內容為未定義。

</dd> </dl>

## <a name="return-value"></a>傳回值

成功時傳回 0;否則，會傳回錯誤。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8.1<br/>                                                                                  |
| 最低支援的伺服器<br/> | Windows Server 2012 R2<br/>                                                                       |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CIM \_ USBDevice**](cim-usbdevice.md)
</dt> </dl>

 

 




