---
title: DTCPIPPort 屬性
description: DTCPIPPort 屬性是一種傳輸控制通訊協定， (TCP) 電腦或裝置的埠號碼，必須透過網際網路通訊協定連線內容保護電腦或裝置， (DTCP-IP) 已驗證的金鑰 Exchange (確定) 作為媒體專案。
ms.assetid: 63767ec1-dd01-40c2-bf9a-6e9b8a7db7f8
keywords:
- DTCPIPPort 屬性 Windows Media Player
topic_type:
- apiref
api_name:
- DTCPIPPort Attribute
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb888d5b52284c7c3000888cf342b4f2f50d16eef8fe4ecad81444ea44b47009
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117935702"
---
# <a name="dtcpipport-attribute"></a>DTCPIPPort 屬性

**DTCPIPPort** 屬性是一種傳輸控制通訊協定， (TCP) 電腦或裝置的埠號碼，必須透過網際網路通訊協定連線內容保護電腦或裝置， (DTCP-IP) 已驗證的金鑰 Exchange (確定) 作為媒體專案。

## <a name="applies-to"></a>套用至

-   [**音訊專案**](audio-item-attributes.md)
-   [**相片專案**](photo-item-attributes.md)
-   [**播放清單專案**](playlist-attributes-ref.md)
-   [**影片專案**](video-item-attributes.md)

## <a name="remarks"></a>備註

如果這個屬性可用，則會使用 DTCP-IP 來保護媒體專案。

目前使用者的本機文件庫中的媒體專案無法使用這個屬性。 它僅適用于屬於遠端媒體櫃的媒體專案;也就是，由家用網路上的另一位使用者所提供的程式庫。 若要判斷媒體櫃是否為遠端，請呼叫 [**IWMPLibrary：： get \_ 類型**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------|
| 版本<br/> | Windows Media Player 12<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**屬性參考**](attribute-reference.md)
</dt> </dl>

 

 





