---
description: LINEMEDIACONTROL \_ 位旗標常數描述一組媒體資料流程的一般作業。
ms.assetid: 1e8aeda8-2810-462a-bfba-0296d854d9aa
title: 'LINEMEDIACONTROL_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f54c7c83df769eef91afe7c310452c342a855f44391815bbc4429ac07bb6ec92
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119309968"
---
# <a name="linemediacontrol_-constants"></a>LINEMEDIACONTROL \_ 常數

**LINEMEDIACONTROL \_** 位旗標常數描述一組媒體資料流程的一般作業。 這些解釋是由媒體資料流程所決定。 線路裝置必須具有媒體控制功能，任何媒體控制作業都能有效運作。

<dl> <dt>

<span id="LINEMEDIACONTROL_NONE"></span><span id="linemediacontrol_none"></span>**LINEMEDIACONTROL \_ 無**
</dt> <dd> <dl> <dt>



媒體資料流程不會進行任何變更。


</dt> </dl> </dd> <dt>

<span id="LINEMEDIACONTROL_PAUSE"></span><span id="linemediacontrol_pause"></span>**LINEMEDIACONTROL \_ 暫停**
</dt> <dd> <dl> <dt>



暫時暫停媒體串流。

媒體資料流程的速度會恢復正常。


</dt> </dl> </dd> <dt>

<span id="LINEMEDIACONTROL_RATEDOWN"></span><span id="linemediacontrol_ratedown"></span>**LINEMEDIACONTROL \_ RATEDOWN**
</dt> <dd> <dl> <dt>



媒體資料流程的速度會隨著部分資料流程定義數量而減少。


</dt> </dl> </dd> <dt>

<span id="LINEMEDIACONTROL_RATENORMAL"></span><span id="linemediacontrol_ratenormal"></span>**LINEMEDIACONTROL \_ RATENORMAL**
</dt> <dd> <dl> <dt>


</dt> </dl> </dd> <dt>

<span id="LINEMEDIACONTROL_RATEUP"></span><span id="linemediacontrol_rateup"></span>**LINEMEDIACONTROL \_ RATEUP**
</dt> <dd> <dl> <dt>



媒體資料流程的速度會隨著部分資料流程定義數量而增加。


</dt> </dl> </dd> <dt>

<span id="LINEMEDIACONTROL_RESET"></span><span id="linemediacontrol_reset"></span>**LINEMEDIACONTROL \_ 重設**
</dt> <dd> <dl> <dt>



重設媒體資料流程。 相當於輸入結尾。 釋放所有緩衝區。


</dt> </dl> </dd> <dt>

<span id="LINEMEDIACONTROL_RESUME"></span><span id="linemediacontrol_resume"></span>**LINEMEDIACONTROL \_ RESUME**
</dt> <dd> <dl> <dt>



繼續已暫停的媒體串流。


</dt> </dl> </dd> <dt>

<span id="LINEMEDIACONTROL_START"></span><span id="linemediacontrol_start"></span>**LINEMEDIACONTROL \_ 開始**
</dt> <dd> <dl> <dt>



啟動媒體資料流程。


</dt> </dl> </dd> <dt>

<span id="LINEMEDIACONTROL_VOLUMEDOWN"></span><span id="linemediacontrol_volumedown"></span>**LINEMEDIACONTROL \_ VOLUMEDOWN**
</dt> <dd> <dl> <dt>



媒體資料流程的波幅會依部分資料流程定義數量而減少。


</dt> </dl> </dd> <dt>

<span id="LINEMEDIACONTROL_VOLUMENORMAL"></span><span id="linemediacontrol_volumenormal"></span>**LINEMEDIACONTROL \_ VOLUMENORMAL**
</dt> <dd> <dl> <dt>



媒體資料流程的波幅會恢復正常。


</dt> </dl> </dd> <dt>

<span id="LINEMEDIACONTROL_VOLUMEUP"></span><span id="linemediacontrol_volumeup"></span>**LINEMEDIACONTROL \_ VOLUMEUP**
</dt> <dd> <dl> <dt>



媒體資料流程的波幅會依部分資料流程定義數量來增加。


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>備註

您可以為裝置專屬的延伸模組指派高序位16位。 低序位16位是保留的。

提供媒體控制項來改善媒體資料流程上動作的效能，以回應電話語音相關事件。 應用程式通常應該透過媒體專屬的 API 來管理媒體串流。 此處提供的媒體控制功能不適合用來取代原生媒體 Api。

媒體控制動作可以與數位偵測、聲音偵測、轉換成通話狀態，以及偵測媒體類型相關聯。 請參閱行的裝置功能，以判斷是否可在線上使用媒體控制項。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 2.0 或更新版本<br/>                                             |
| 標頭<br/>       | <dl> <dt>Tapi</dt> </dl> |



 

 




