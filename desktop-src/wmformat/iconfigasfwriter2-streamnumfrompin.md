---
title: IConfigAsfWriter2 StreamNumFromPin 方法
description: StreamNumFromPin 方法會抓取與指定之輸入 pin 相關聯的資料流程號碼。
ms.assetid: f645a742-e6dc-4041-8a56-3bbb5188a9a9
keywords:
- StreamNumFromPin 方法 windows Media 格式
- StreamNumFromPin 方法 windows Media Format，IConfigAsfWriter2 介面
- IConfigAsfWriter2 介面 windows Media Format，StreamNumFromPin 方法
topic_type:
- apiref
api_name:
- IConfigAsfWriter2.StreamNumFromPin
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c63a31d515e70b0ee0ac5be617ee52fe23bd5416
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375588"
---
# <a name="iconfigasfwriter2streamnumfrompin-method"></a>IConfigAsfWriter2：： StreamNumFromPin 方法

**StreamNumFromPin** 方法會抓取與指定之輸入 pin 相關聯的資料流程號碼。

## <a name="syntax"></a>語法


```C++
HRESULT StreamNumFromPin(
  [in]  IPin *pPin,
  [out] WORD *pwStreamNum
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pPin* \[在\]
</dt> <dd>

輸入釘選上 **IPin** 介面的指標。

</dd> <dt>

*pwStreamNum* \[擴展\]
</dt> <dd>

接收資料流程號碼的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果方法成功，它會傳回 S \_ OK。 如果失敗，則會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

有時，您可能需要直接使用 Windows Media Format SDK 介面來運算元據流，才能執行篩選圖形。 因為您無法假設 ASF 串流號碼與 DirectShow pin 碼相同，所以會提供這個方法。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IConfigAsfWriter2 介面**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))
</dt> </dl>

 

 