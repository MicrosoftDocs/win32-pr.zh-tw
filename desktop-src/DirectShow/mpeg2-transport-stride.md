---
description: MPEG2 \_ 傳輸 \_ STRIDE 結構說明 mpeg-2 傳輸串流 (TS) 封包的格式。
ms.assetid: 269d5fba-2dea-4786-93d6-e52b56c8bb53
title: 'MPEG2_TRANSPORT_STRIDE 結構 (Bdatypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MPEG2_TRANSPORT_STRIDE
api_type:
- HeaderDef
api_location:
- bdatypes.h
ms.openlocfilehash: 4a0cdc21bdd8c320728da0c0af8c0af023de68eb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981270"
---
# <a name="mpeg2_transport_stride-structure"></a>MPEG2 \_ 傳輸 \_ STRIDE 結構

`MPEG2_TRANSPORT_STRIDE`結構描述 mpeg-2 傳輸串流 (TS) 封包的格式。 此結構允許傳輸資料流程，其中188位元組傳輸封包不是連續的。 基於本檔的目的，這類封包稱為 stride 封 *包*。

Stride 封包是由下列媒體類型來識別：



|             |                                        |
|-------------|----------------------------------------|
| 主要類型  | 媒體媒體的 \_ 串流                      |
| Subtype     | MEDIASUBTYPE \_ MPEG2 \_ 傳輸 \_ STRIDE |
| 格式類型 | 格式化 \_ 無                           |



 

格式區塊 (**pbFormat**) 是選擇性的。 如果包含格式區塊，則必須以 **MPEG2 \_ 傳輸 \_ STRIDE** 結構作為開頭。 此結構會定義 stride 封包內傳輸封包的版面配置。 如果格式區塊為 **Null**，則會假設封包使用一組預設值;如需詳細資訊，請參閱「備註」一節。

## <a name="syntax"></a>語法


```C++
typedef struct _MPEG2_TRANSPORT_STRIDE {
  DWORD dwOffset;
  DWORD dwPacketLength;
  DWORD dwStride;
} MPEG2_TRANSPORT_STRIDE, *PMPEG2_TRANSPORT_STRIDE;
```



## <a name="members"></a>成員

<dl> <dt>

**dwOffset**
</dt> <dd>

指定從封包開頭到內嵌傳輸封包第一個位元組的位移（以位元組為單位）。 值的範圍必須介於零到 `(dwStride - dwPacketLength)` （含）之間。

</dd> <dt>

**dwPacketLength**
</dt> <dd>

指定內嵌傳輸封包的長度（以位元組為單位）。 若為標準的 MPEG-2 傳輸封包，此值必須為188個位元組。

</dd> <dt>

**dwStride**
</dt> <dd>

指定整個 stride 封包的長度（以位元組為單位）。 值必須至少為 `(dwOffset + dwPacketLength)` 。

</dd> </dl>

## <a name="remarks"></a>備註

下圖說明結構成員之間的關聯性。

![mpeg-2 stride 封包](images/mpeg2-stride-packet.png)

包含多工跨距封包的輸入緩衝區有一些限制：

-   Stride 封包必須連續封裝在緩衝區內。
-   第一個 stride 封包之前沒有任何位元組，或遵循最後一個 stride 封包。
-   緩衝區中的 stride 封包數目必須符合;也就是說，緩衝區長度% dwStride 等於零。

每個緩衝區的 stride 封包數目沒有任何限制。

如果媒體類型不包含格式區塊 (**pbFormat** 為 **Null**) ，則會使用下列預設值：

-   **dwOffset**：0
-   **dwPacketLength**：188
-   **dwStride**：188

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Bdatypes。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[DirectShow 結構](directshow-structures.md)
</dt> <dt>

[MPEG-2 媒體類型](mpeg-2-media-types.md)
</dt> </dl>

 

 




