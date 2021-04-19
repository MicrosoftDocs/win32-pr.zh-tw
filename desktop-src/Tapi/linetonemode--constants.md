---
description: LINETONEMODE \_ 常數描述產生換行時所使用的不同選項。
ms.assetid: 7bfc7d4e-2ab3-44ec-a936-f2d7dcfce263
title: 'LINETONEMODE_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9e1b5a8d49c927dfa3d5ec87f9a4830a91d79d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995624"
---
# <a name="linetonemode_-constants"></a>LINETONEMODE \_ 常數

**LINETONEMODE \_ 常數** 描述產生換行時所使用的不同選項。

<dl> <dt>

<span id="LINETONEMODE_BEEP"></span><span id="linetonemode_beep"></span>**LINETONEMODE \_ 嗶聲**
</dt> <dd> <dl> <dt>



色調是一種嗶聲，例如用來宣佈錄製開頭的聲提示。 確切定義是定義的服務提供者。


</dt> </dl> </dd> <dt>

<span id="LINETONEMODE_BILLING"></span><span id="linetonemode_billing"></span>**LINETONEMODE \_ 帳單**
</dt> <dd> <dl> <dt>



語氣是帳單資訊語氣，例如信用卡提示音。 確切定義是定義的服務提供者。


</dt> </dl> </dd> <dt>

<span id="LINETONEMODE_BUSY"></span><span id="linetonemode_busy"></span>**LINETONEMODE \_ 忙碌**
</dt> <dd> <dl> <dt>



色調是忙碌的聲音。 確切定義是定義的服務提供者。


</dt> </dl> </dd> <dt>

<span id="LINETONEMODE_CUSTOM"></span><span id="linetonemode_custom"></span>**LINETONEMODE \_ 自訂**
</dt> <dd> <dl> <dt>



色調是由其元件頻率定義的自訂色調，其類型為 [**LINEGENERATETONE**](/windows/desktop/api/Tapi/ns-tapi-linegeneratetone)。


</dt> </dl> </dd> <dt>

<span id="LINETONEMODE_RINGBACK"></span><span id="linetonemode_ringback"></span>**LINETONEMODE \_ 回電**
</dt> <dd> <dl> <dt>



語氣是回電語氣。 確切定義是定義的服務提供者。


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>備註

您可以為裝置專屬的延伸模組指派高序位16位。 低序位16位是保留的。

這些常數用來定義透過呼叫遠端方所產生的聲音 inband。 請注意，非自訂色調的色調偵測不會使用這些常數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 2.0 或更新版本<br/>                                             |
| 標頭<br/>       | <dl> <dt>Tapi</dt> </dl> |



 

 




