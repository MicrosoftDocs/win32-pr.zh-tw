---
title: SRStatus 屬性
description: SRStatus 屬性
ms.assetid: 67618a35-05e4-4bb3-b910-c75de6e32578
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d7cc079c79b3539fa5ad90da4f45907236f19d3b841cf580142446b230ff7c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975678"
---
# <a name="srstatus-property"></a>SRStatus 屬性

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**
</dt> <dd>

傳回是否可針對字元啟動語音輸入。

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**
</dt> <dd>

*agent. ***字元 ( "**_CharacterID_*_" ) 。SRStatus_*



| 值 | 描述                                                                                                                                                                                                                               |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | 條件支援語音輸入。                                                                                                                                                                                                          |
| 1     | 此系統上沒有可用的音訊輸入裝置。  (請注意，這不會偵測是否已安裝麥克風;它只能偵測使用者是否已安裝具有正常運作驅動程式的已啟用輸入的音效卡。 )  |
| 2     | 另一個用戶端是此字元的作用中用戶端，或目前的字元不是最上層。                                                                                                                                           |
| 3     | 音訊輸入或輸出通道目前忙碌中，應用程式正在使用音訊。                                                                                                                                                       |
| 4     | 初始化語音辨識子系統的過程中發生未指定的錯誤。 這包括沒有任何語音引擎可符合字元語言設定的可能性。                          |
| 5     | 使用者已停用 Advanced Character 選項中的語音輸入。                                                                                                                                                                     |
| 6     | 檢查音訊狀態時發生錯誤，但系統不會傳回錯誤的原因。                                                                                                                                |



 

</dd> </dl>

## <a name="remarks"></a>備註

這個屬性會傳回支援語音輸入所需的條件，包括音訊裝置的狀態。 您可以先檢查這個屬性，然後再呼叫 [**接聽**](listen-method.md) 方法，以更妥善地確保其成功。

在 [代理程式] 屬性工作表中啟用語音輸入時 ([Advanced Character Options]) ，查詢此屬性將會載入相關聯的引擎（如果尚未載入），並啟動語音服務。 亦即，接聽鍵可供使用，而且接聽提示會自動顯示。  (接聽金鑰和接聽提示只會在 [高階字元選項] 中啟用時才會啟用 ) 。不過，如果您在停用語音時查詢屬性，伺服器就不會啟動語音服務。

這個屬性只適用于用戶端應用程式使用的字元;此設定不會影響用戶端應用程式中其他字元或其他字元的用戶端。

## <a name="see-also"></a>另請參閱

[**接聽方法**](listen-method.md)


 

 




