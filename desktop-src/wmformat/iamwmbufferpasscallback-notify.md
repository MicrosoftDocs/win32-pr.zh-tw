---
title: IAMWMBufferPassCallback Notify 方法
description: 在串流處理期間傳遞的每個緩衝區，會呼叫通知方法。
ms.assetid: 3f252754-c784-4ffd-bcfc-fab73fa02b9a
keywords:
- 通知方法 windows Media 格式
- 通知方法 windows Media 格式，IAMWMBufferPassCallback 介面
- IAMWMBufferPassCallback 介面 windows Media Format，Notify 方法
topic_type:
- apiref
api_name:
- IAMWMBufferPassCallback.Notify
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f364243e40400884287c6219698991ccf8afc0be86a85ec612a5b193253994dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117847533"
---
# <a name="iamwmbufferpasscallbacknotify-method"></a>IAMWMBufferPassCallback：： Notify 方法

在串流處理期間傳遞的每個緩衝區，會呼叫 **通知** 方法。

## <a name="syntax"></a>語法


```C++
HRESULT Notify(
  [in] INSSBuffer3    *pNSSBuffer3,
  [in] IPin           *pPin,
  [in] REFERENCE_TIME *prtStart,
  [in] REFERENCE_TIME *prtEnd
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pNSSBuffer3* \[在\]
</dt> <dd>

媒體範例上公開的 [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) 介面指標。

</dd> <dt>

*pPin* \[在\]
</dt> <dd>

與範例所屬之媒體資料流程相關聯的釘選指標。

</dd> <dt>

*prtStart* \[在\]
</dt> <dd>

範例的開始時間。

</dd> <dt>

*prtEnd* \[在\]
</dt> <dd>

範例的結束時間。

</dd> </dl>

## <a name="return-value"></a>傳回值

未指定任何特定的傳回值。 呼叫的 pin 會忽略 **HRESULT**。

## <a name="remarks"></a>備註

這個方法可讓應用程式在處理緩衝區內容之前，先檢查媒體緩衝區中的資訊並採取行動。 應用程式會負責瞭解 pin 上的媒體類型。 您可以先從設定檔取得串流資訊，然後呼叫 [**IConfigAsfWriter2：： StreamNumFromPin**](iconfigasfwriter2-streamnumfrompin.md) 方法來判斷哪個 pin 與每個資料流程相關聯，藉以取得這項資訊。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**DirectShowQASF 參考**](directshow-qasf-reference.md)
</dt> <dt>

[**IAMWMBufferPassCallback 介面**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpasscallback)
</dt> <dt>

[**INSSBuffer3 介面**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3)
</dt> </dl>

 

 