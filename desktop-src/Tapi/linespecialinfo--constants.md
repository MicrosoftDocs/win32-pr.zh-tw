---
description: LINESPECIALINFO \_ 位旗標常數描述網路可用來報告各種報告和網路觀察作業的特殊資訊信號。
ms.assetid: b94f8a6f-b84d-4976-b4d4-10dee5a1a4d8
title: 'LINESPECIALINFO_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78154757515ebd5bfa36778795c26ef9fdc96db1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989559"
---
# <a name="linespecialinfo_-constants"></a>LINESPECIALINFO \_ 常數

**LINESPECIALINFO \_** 位旗標常數描述網路可用來報告各種報告和網路觀察作業的特殊資訊信號。 它們是在網路諮詢記錄的公告開頭傳送的特殊編碼語氣序列。

<dl> <dt>

<span id="LINESPECIALINFO_CUSTIRREG"></span><span id="linespecialinfo_custirreg"></span>**LINESPECIALINFO \_ CUSTIRREG**
</dt> <dd> <dl> <dt>



這項特殊資訊語氣優先于空白號碼、AIS、Centrex 數位變更和非工作站、存取程式碼未撥打或撥入錯誤，或手動攔截操作員訊息 (客戶 irregularity 類別) 。 \_當帳單資訊遭到拒絕，以及在切換時封鎖撥號位址時，也會回報 LINESPECIALINFO CUSTIRREG。


</dt> </dl> </dd> <dt>

<span id="LINESPECIALINFO_NOCIRCUIT"></span><span id="linespecialinfo_nocircuit"></span>**LINESPECIALINFO \_ NOCIRCUIT**
</dt> <dd> <dl> <dt>



這種特殊資訊語氣會在沒有線路或緊急公告之前 (主幹封鎖類別) 。


</dt> </dl> </dd> <dt>

<span id="LINESPECIALINFO_REORDER"></span><span id="linespecialinfo_reorder"></span>**LINESPECIALINFO \_ 重新排序**
</dt> <dd> <dl> <dt>



這種特殊資訊語氣優先于重新訂購公告 (設備 irregularity 類別) 。 \_當電話保持 offhook 太長時，也會回報 LINESPECIALINFO 重新排序。


</dt> </dl> </dd> <dt>

<span id="LINESPECIALINFO_UNAVAIL"></span><span id="linespecialinfo_unavail"></span>**LINESPECIALINFO \_ UNAVAIL**
</dt> <dd> <dl> <dt>



有關特殊資訊語氣的詳細資料無法使用，也不會變成已知。


</dt> </dl> </dd> <dt>

<span id="LINESPECIALINFO_UNKNOWN"></span><span id="linespecialinfo_unknown"></span>**LINESPECIALINFO \_ 不明**
</dt> <dd> <dl> <dt>



有關特殊資訊語氣的詳細資訊目前不明，但稍後可能會變成已知。


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>備註

您可以為裝置專屬的延伸模組指派高序位16位。 低序位16位是保留的。

系統會針對諮詢訊息定義特殊的資訊色調，而且通常不會用於計費或監督用途。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 2.0 或更新版本<br/>                                             |
| 標頭<br/>       | <dl> <dt>Tapi</dt> </dl> |



 

 




