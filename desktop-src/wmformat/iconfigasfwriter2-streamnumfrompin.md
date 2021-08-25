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
ms.openlocfilehash: 9124d3acaea81e36b212f3dec001374cc035efca449f35af5e43fa18ce50d6dd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119839819"
---
# <a name="iconfigasfwriter2streamnumfrompin-method"></a>IConfigAsfWriter2：： StreamNumFromPin 方法

**StreamNumFromPin** 方法會抓取與指定之輸入 pin 相關聯的資料流程號碼。

## <a name="syntax"></a>語法


```C++
HRESULT StreamNumFromPin(
  [in]  IPin *pPin,
  [out] WORD *pwStreamNum
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

有時您可能需要直接使用 Windows 媒體格式 SDK 介面，以在執行篩選圖形之前操控資料流程。 因為您無法假設 ASF 資料流程號碼與 DirectShow pin 號碼相同，所以會提供這個方法。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IConfigAsfWriter2 介面**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))
</dt> </dl>

 

 