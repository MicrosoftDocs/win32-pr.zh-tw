---
description: 以 mb 為單位指定配量的大小 (MB) 、位或 MB 的資料列。
ms.assetid: 42E7DB19-9FB9-4226-B0B5-97AD6B9C0E12
title: 'CODECAPI_AVEncSliceControlSize 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e4c3e58fa34922941ea564d42e449cefd798ad2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111861"
---
# <a name="codecapi_avencslicecontrolsize-property"></a>CODECAPI \_ AVEncSliceControlSize 屬性

以 mb 為單位指定配量的大小 (MB) 、位或 MB 的資料列。

## <a name="data-type"></a>資料類型

**ULONG** (VT \_ UI4) 

## <a name="property-guid"></a>屬性 GUID

**CODECAPI \_ AVEncSliceControlSize**

## <a name="remarks"></a>備註

**H.264/AVC 編碼器：**

CODECAPI AVEncSliceControlSize 值的意義 \_ 是由 [CODECAPI \_ AVEncSliceControlMode](codecapi-avencslicecontrolmode.md) 屬性所控制。 下表說明 CODECAPI \_ AVEncSliceControlSize 和 CODECAPI \_ AVEncSliceControlMode 屬性如何控制框架中的磁區大小和數目。



| CODECAPI \_ AVEncSliceControlMode 設定 | 值的意義                                                                                                                                                                                                                                                                                                                                                                                           |
|-----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0                                       | 這是一個整數，指出框架中每個配量的大小（以巨大區塊為單位）。 <br/> 當值大於框架中的巨大區塊數目時，編碼器應該拒絕設定。<br/>                                                                                                                                                                         |
| 1                                       | 這是一個整數，指出框架中每個磁區的大小（以位為單位）。 <br/> 編碼器應該會在巨大區塊上啟動新的配量，此配量會導致配量中的位數超過此值 (因此，每個配量的大小一律會小於或等於此值) 。 這表示最後一個配量大小可能明顯小於此值。 <br/> |
| 2                                       | 這是一個整數，以巨大區塊資料列的單位表示框架中每個配量的大小。 <br/> 當值大於框架中的巨大區塊資料列數目時，編碼器應該拒絕設定。<br/>                                                                                                                                                                 |



 

如果應用程式未設定 [CODECAPI \_ AVEncSliceControlMode](codecapi-avencslicecontrolmode.md)的值，則編碼器應該會傳回錯誤。

建議的預設值是針對整個框架具有單一配量。

某些編碼器可能會以平行方式編碼配量，因此效能可能會受到影響，取決於配量控制項設定。 例如，將框架編碼成單一配量可能會比框架編碼為多個配量更慢。

配量控制項設定為動態，而且可以在編碼會話期間變更。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8.1 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                                   |
| 最低支援的伺服器<br/> | Windows Server 2012 R2 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                        |
| 標頭<br/>                   | <dl> <dt>Codecapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎屬性](media-foundation-properties.md)
</dt> </dl>

 

 




