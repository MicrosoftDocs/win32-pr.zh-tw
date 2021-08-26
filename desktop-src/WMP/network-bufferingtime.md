---
title: BufferingTime
description: BufferingTime 屬性會指定或抓取在開始播放之前，為了緩衝處理傳入資料所配置的時間量（以毫秒為單位）。
ms.assetid: b52b7f44-6be1-4299-94da-c37d758795af
keywords:
- BufferingTime Windows Media Player
topic_type:
- apiref
api_name:
- Network.bufferingTime
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: afe4a68a7ad1ae8a1444f1e2f31ad09461e05d221e8fceae52960bd5927aac0c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119901728"
---
# <a name="networkbufferingtime"></a>BufferingTime

**BufferingTime** 屬性會指定或抓取在開始播放之前，為了緩衝處理傳入資料所配置的時間量（以毫秒為單位）。

## <a name="syntax"></a>Syntax

*玩家*。*網路*。**bufferingTime**

## <a name="possible-values"></a>可能的值

此屬性是讀取/寫入 **號碼** (**長**) 範圍從零到60000，預設值是5000。

## <a name="examples"></a>範例

下列 JScript 範例會使用 *網路*。**bufferingTime** ，指定配置給緩衝傳入資料的秒數。 系統會從以 ID = "bufText" 建立的 HTML 文字輸入元素抓取資訊。 使用 ID = "Player" 建立 **player** 物件。


```JScript
<!-- Create a BUTTON element to change the bufferingTime value. -->
<INPUT TYPE = "BUTTON" NAME = "bufTime" ID = "bufTime" 
       VALUE = "Change Buffer Time"

    onClick = "
       /* Test whether the user entered a valid value. */
       if (bufText.value >= 0 & bufText.value <= 60) 
           Player.network.bufferingTime = bufText.value * 1000;
       else
           alert('Buffering time must be between 0 and 60.');
">

```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本。<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Network 物件**](network-object.md)
</dt> </dl>

 

 





