---
description: LINECONNECTEDMODE \_ 位旗標常數描述連接呼叫的不同 substates。
ms.assetid: d75a5989-3f4e-4e5d-90b1-4e450def017e
title: 'LINECONNECTEDMODE_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5191d3a575ef353c54c91c0e53b3228621b703cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998848"
---
# <a name="lineconnectedmode_-constants"></a>LINECONNECTEDMODE \_ 常數

**LINECONNECTEDMODE \_** 位旗標常數描述連接呼叫的不同 substates。 在撥號狀態轉換為已連線，且在 \_ 指出呼叫在 LINECALLSTATE 連線中的行 CALLSTATE 訊息內，可以使用模式作為應用程式的撥號狀態 \_ 。 當呼叫位於與其他工作站 (橋接) 的共用位址時，就會使用這些值 (如需詳細資訊，請參閱 [**LINEADDRESSSHARING \_ 常數**](lineaddresssharing--constants.md)) ，主要是電子關鍵系統。 **LINECONNECTEDMODE \_ 常數** 具有下列值：

<dl> <dt>

<span id="LINECONNECTEDMODE_ACTIVE"></span><span id="lineconnectedmode_active"></span>**LINECONNECTEDMODE \_ 使用中**
</dt> <dd> <dl> <dt>



指出呼叫是在目前工作站上連接 (目前的工作站是呼叫) 中的參與者。 如果撥號狀態模式為 0 (零) ，應用程式應該假設值為「作用中」 (這會是非橋接位址) 上的情況。 如果使用者加入並透過手動動作離開通話，則模式可以在呼叫期間于作用中和非作用中切換。 在這種橋接的情況下， [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop) 或 [**lineHold**](/windows/desktop/api/Tapi/nf-tapi-linehold) 作業可能不會實際卸載或放置通話，因為來電中其他工作站的狀態可能會控制 (例如，當其他工作站參與時，嘗試「保留」來電是不可能的) ;相反地，如果呼叫仍在其他工作站上連線，則可能會變更為非作用中模式。


</dt> </dl> </dd> <dt>

<span id="LINECONNECTEDMODE_ACTIVEHELD"></span><span id="lineconnectedmode_activeheld"></span>**LINECONNECTEDMODE \_ ACTIVEHELD**
</dt> <dd> <dl> <dt>



指出工作站是呼叫中的作用中參與者，但遠端合作物件已將呼叫放置在待命 (另一方將) 的呼叫視為處於舉 servicerequeststatusenum.onhold 狀態。 一般來說，只有當呼叫的兩個端點落在相同的切換網域內時，才會提供這類資訊。 此旗標只會公開給協調 TAPI 2.0 版或更新版本的應用程式。  (TAPI 2.0 版和更新版本) 


</dt> </dl> </dd> <dt>

<span id="LINECONNECTEDMODE_CONFIRMED"></span><span id="lineconnectedmode_confirmed"></span>**LINECONNECTEDMODE \_ 確認**
</dt> <dd> <dl> <dt>



指出服務提供者收到肯定通知，指出呼叫已進入線上狀態 (例如，透過回答監督或類似的機制) 。 此旗標只會公開給協調 TAPI 2.0 版或更新版本的應用程式。  (TAPI 2.0 版和更新版本) 


</dt> </dl> </dd> <dt>

<span id="LINECONNECTEDMODE_INACTIVE"></span><span id="lineconnectedmode_inactive"></span>**LINECONNECTEDMODE \_ 非使用中**
</dt> <dd> <dl> <dt>



指出呼叫在一或多個其他工作站上為作用中，但目前的工作站不是呼叫中的參與者。 如果撥號狀態模式為零，則應用程式應該假設值為「作用中」 (這會是非橋接位址) 上的情況。 處於非使用中狀態的呼叫可以使用 [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer)聯結。 許多在連接狀態下都有效的作業，可能無法在非使用中的模式下使用，例如監視音調和數位，因為工作站實際上並未參與呼叫;當呼叫處於非使用中模式時，監視通常會暫停 (但未取消) 。


</dt> </dl> </dd> <dt>

<span id="LINECONNECTEDMODE_INACTIVEHELD"></span><span id="lineconnectedmode_inactiveheld"></span>**LINECONNECTEDMODE \_ INACTIVEHELD**
</dt> <dd> <dl> <dt>



指出此工作站不是呼叫中的作用中參與者，而且遠端方已將呼叫置於待命狀態。 此旗標只會公開給協調 TAPI 2.0 版或更新版本的應用程式。  (TAPI 2.0 版和更新版本) 


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>備註

不可延伸。 所有32位都是保留的。

為了回溯相容性，服務提供者必須負責檢查該行上的已協商 API 版本，而且不會使用 \_ 經過協商的版本不支援的 LINECONNECTEDMODE 值。 未 cognizant LINECONNECTEDMODE 的應用程式 \_ 很有可能會假設 LINECALLSTATE 連接的呼叫位於 \_ LINECONNECTEDMODE \_ ACTIVE 中。

\_ \_ 當呼叫位於與其他工作站共用 (橋接的位址時，會使用 LINECONNECTEDMODE ACTIVE 和 LINECONNECTEDMODE 非使用中的值; 請參閱 [**LINEADDRESSSHARING \_ 常數**](lineaddresssharing--constants.md)) ，主要是電子金鑰系統。 如果連接的撥號狀態模式為「作用中」，這表示呼叫是在目前的工作站上連接 (目前的工作站是呼叫中的參與者) 。 如果通話狀態模式為「非使用中」，則會在一或多個其他工作站上使用中的呼叫，但目前的工作站不是呼叫的參與者。 如果撥號狀態模式為零，則應用程式應該假設值為「作用中」 (這會是非橋接位址) 上的情況。 如果使用者加入並透過手動動作離開通話，則模式可以在呼叫期間于作用中和非作用中切換。

在這種橋接的情況下， [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop) 或 [**lineHold**](/windows/desktop/api/Tapi/nf-tapi-linehold) 作業可能不會實際卸載或放置通話，因為來電中其他工作站的狀態可能會控制 (例如，在其他工作站參與時嘗試「保留」來電將無法) ;相反地，呼叫可以直接變更為非作用中模式（如果它仍在其他工作站上連線）。 處於非使用中狀態的呼叫可以使用 [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer)聯結。

許多在連接狀態下都有效的作業，可能無法在非使用中的模式下使用，例如監視音調和數位，因為工作站實際上並未參與呼叫;當呼叫處於非使用中模式時，監視通常會暫停 (但未取消) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 2.0 或更新版本<br/>                                             |
| 標頭<br/>       | <dl> <dt>Tapi</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer)
</dt> <dt>

[**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop)
</dt> <dt>

[**lineHold**](/windows/desktop/api/Tapi/nf-tapi-linehold)
</dt> </dl>

 

 




