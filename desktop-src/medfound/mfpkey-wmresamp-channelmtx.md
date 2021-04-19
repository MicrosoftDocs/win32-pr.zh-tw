---
description: 指定通道矩陣，用來將來源通道轉換成目的通道 (例如，將5.1 轉換成身歷聲) 。
ms.assetid: 2f2a82bd-f051-4b05-a9c8-37aa4403fab4
title: 'MFPKEY_WMRESAMP_CHANNELMTX 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e39f9a9344dd080362859592fcf1f71657ee8f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106979078"
---
# <a name="mfpkey_wmresamp_channelmtx-property"></a>MFPKEY \_ WMRESAMP \_ CHANNELMTX 屬性

指定通道矩陣，用來將來源通道轉換成目的通道 (例如，將5.1 轉換成身歷聲) 。

## <a name="constant-for-ipropertybag"></a>IPropertyBag 的常數

僅可使用 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)。

## <a name="data-type"></a>資料類型

VT \_ I4 \| vt \_ 陣列

## <a name="applies-to"></a>套用至

-   [音訊 Resampler DSP](audioresampler.md)

## <a name="remarks"></a>備註

屬性的值是 Ns x Nd 係數的矩陣，其中 Ns 是來源通道的數目，Nd 是目的地通道的數目。 係數會以分貝指定，使用下列公式：

 (int)  (65536 \* 20 \* Log10 (dB) ) 

矩陣會以資料列主要順序的形式儲存，其中的資料列編號是來源通道，而資料行編號則是目的地通道。

因此，如果矩陣如下所示：

``` syntax
00       01       ...      0(Ns-1)
10       11       ...      1(Ns-1)
...      ...      ...      ...
(Nd-1)0 (Nd-1)1 ... (Nd-1)(Ns-1)
```

然後，您會將陣列指定為：

``` syntax
[ 00, 01, ..., 0(Ns-1), 10, 11, ..., 1(Ns-1), ..., (Nd-1)0, (Nd-1)1, ..., (Nd-1)(Ns-1) ]
```

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                    |
| 標頭<br/>                   | <dl> <dt>Wmcodecdsp。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎屬性](media-foundation-properties.md)
</dt> </dl>

 

 
