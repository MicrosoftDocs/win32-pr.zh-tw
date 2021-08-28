---
description: Windows可攜式裝置支援下列音訊屬性。
ms.assetid: 5d6c6a95-abb7-4191-a961-bcb30ca96bb6
title: '音訊屬性 (PortableDevice .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Audio
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 93ddbee0eb078c1b9d5a1e7c64288e95b47e2bdb0363bf8b7b19cb773129d0ba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119590408"
---
# <a name="audio-properties"></a>音訊屬性

Windows可攜式裝置支援下列音訊屬性。



| 屬性                         | VarType     | 描述                                                                                                                                                                                                        |
|----------------------------------|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **WPD \_ 音訊 \_ 位 \_ 深度**       | **VT \_ UI4** | 音訊的位深度。                                                                                                                                                                                        |
| **WPD \_ 音訊 \_ 位元速率**          | **VT \_ UI4** | 音訊的位元速率，以位/秒為單位。                                                                                                                                                                     |
| **WPD \_ 音訊 \_ 區塊 \_ 對齊** | **VT \_ UI4** | 音訊檔案的區塊對齊（以位元組為單位）。                                                                                                                                                                   |
| **WPD \_ 音訊 \_ 頻道 \_ 計數**   | **VT \_ R4**  | 此音訊檔案中的通道數目，例如1、2或5.1。                                                                                                                                              |
| **WPD \_ 音訊 \_ 格式 \_ 代碼**     | **VT \_ UI4** | 註冊的 WAVE 格式代碼編號。 如需註冊的 WAVE 格式清單，請參閱 MSDN 網站上的 [註冊的 FOURCC 碼和 WAVE 格式](https://msdn2.microsoft.com/library/ms867195.aspx) 文章。 |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>PortableDevice。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**WPD 屬性和屬性**](properties-and-attributes.md)
</dt> </dl>

 

 




