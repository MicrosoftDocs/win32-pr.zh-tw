---
description: LINEADDRCAPFLAGS \_ 位旗標常數用於 LINEADDRESSCAPS 資料結構的 dwAddrCapFlags 成員，以描述各種布林值位址功能。
ms.assetid: 530af273-82ba-4310-8aac-266d657e1bfe
title: 'LINEADDRCAPFLAGS_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27ce6c8bebb5683d5ecb7d576ff7d376ad0d62cc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001812"
---
# <a name="lineaddrcapflags_-constants"></a>LINEADDRCAPFLAGS \_ 常數

**LINEADDRCAPFLAGS** \_ 位旗標常數用於 [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)資料結構的 **DwAddrCapFlags** 成員，以描述各種布林值位址功能。

<dl> <dt>

<span id="LINEADDRCAPFLAGS_ACCEPTTOALERT"></span><span id="lineaddrcapflags_accepttoalert"></span>**LINEADDRCAPFLAGS \_ ACCEPTTOALERT**
</dt> <dd> <dl> <dt>



**如果必須** 使用 [**lineAccept**](/windows/desktop/api/Tapi/nf-tapi-lineaccept) 接受供應專案呼叫，請使用此專案來開始在呼叫的兩端發出警示的使用者。否則 **為 FALSE**。 這通常僅適用于 ISDN。


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_ACDGROUP"></span><span id="lineaddrcapflags_acdgroup"></span>**LINEADDRCAPFLAGS \_ ACDGROUP**
</dt> <dd> <dl> <dt>



此位址支援與撥接中心作業連接的 [ACD 群組](about-call-center-controls.md#acd-group-object) 。 如需 ACD 群組的詳細資訊，請參閱「 [關於電話中心」控制項](./about-call-center-controls.md) 。


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_AUTORECONNECT"></span><span id="lineaddrcapflags_autoreconnect"></span>**LINEADDRCAPFLAGS \_ AUTORECONNECT**
</dt> <dd> <dl> <dt>



指定卸載諮詢通話是否會自動重新連線到諮詢保留的呼叫。 如果自動重新連線發生，則 **為 TRUE** ;否則 **為 FALSE**。


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_BLOCKIDDEFAULT"></span><span id="lineaddrcapflags_blockiddefault"></span>**LINEADDRCAPFLAGS \_ BLOCKIDDEFAULT**
</dt> <dd> <dl> <dt>



指定當對此位址進行呼叫時，網路預設是否傳送或封鎖呼叫端識別碼資訊。 若 **為 TRUE**，則預設會封鎖識別碼資訊;如果 **為 FALSE**，則預設會傳輸識別碼資訊。


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_BLOCKIDOVERRIDE"></span><span id="lineaddrcapflags_blockidoverride"></span>**LINEADDRCAPFLAGS \_ BLOCKIDOVERRIDE**
</dt> <dd> <dl> <dt>



指定是否可以覆寫每個呼叫的傳送或封鎖呼叫者識別碼資訊的預設設定。 若 **為 TRUE**，則可能覆寫;如果 **為 FALSE**，則表示不可能覆寫。


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_COMPLETIONID"></span><span id="lineaddrcapflags_completionid"></span>**LINEADDRCAPFLAGS \_ COMPLETIONID**
</dt> <dd> <dl> <dt>



指定 [**lineCompleteCall**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall) 傳回的完成識別碼是否有用且不重複。 如果有用處，**則為 TRUE** ;否則 **為 FALSE**。


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_CONFDROP"></span><span id="lineaddrcapflags_confdrop"></span>**LINEADDRCAPFLAGS \_ CONFDROP**
</dt> <dd> <dl> <dt>



如果在會議呼叫父系上的 [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop)也具有卸載 (也就是中斷與參與會議通話的其他合作物件) 的副作用，則 **為 TRUE** 。如果卸載會議通話仍允許其他人在彼此之間交談，則 **為 FALSE** 。


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_CONFERENCEHELD"></span><span id="lineaddrcapflags_conferenceheld"></span>**LINEADDRCAPFLAGS \_ CONFERENCEHELD**
</dt> <dd> <dl> <dt>



指定是否可以將硬式呼叫 conferenced 至。 通常，只有諮詢保留的呼叫可以新增為會議通話。


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_CONFERENCEMAKE"></span><span id="lineaddrcapflags_conferencemake"></span>**LINEADDRCAPFLAGS \_ CONFERENCEMAKE**
</dt> <dd> <dl> <dt>



指定是否可以建立全新的呼叫，以作為諮詢電話， (在會議上新增) 。


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_DESTOFFHOOK"></span><span id="lineaddrcapflags_destoffhook"></span>**LINEADDRCAPFLAGS \_ DESTOFFHOOK**
</dt> <dd> <dl> <dt>



指定呼叫方的電話是否可以在進行呼叫時自動強制 offhook。


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_DIALED"></span><span id="lineaddrcapflags_dialed"></span>**LINEADDRCAPFLAGS \_ 撥號**
</dt> <dd> <dl> <dt>



指定是否可在此位址上撥打目的地位址以進行呼叫。 如果必須撥打目的地位址，則 **為 TRUE** ;如果目的地位址是固定的，則為 **FALSE** ， (為「熱電話」 ) 。


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_FWDBUSYNAADDR"></span><span id="lineaddrcapflags_fwdbusynaaddr"></span>**LINEADDRCAPFLAGS \_ FWDBUSYNAADDR**
</dt> <dd> <dl> <dt>



指定是否忙碌的呼叫轉送，而且沒有任何答案可以使用不同的轉送位址。 只有在忙碌和沒有答案的轉送可以個別控制時，此旗標才有意義。 如果轉送忙碌且沒有答案可以使用不同的目的地位址，則此旗標為 **TRUE** 。否則為 **FALSE**。


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_FWDCONSULT"></span><span id="lineaddrcapflags_fwdconsult"></span>**LINEADDRCAPFLAGS \_ FWDCONSULT**
</dt> <dd> <dl> <dt>



指定呼叫轉送是否牽涉到建立諮詢電話。


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_FWDINTEXTADDR"></span><span id="lineaddrcapflags_fwdintextaddr"></span>**LINEADDRCAPFLAGS \_ FWDINTEXTADDR**
</dt> <dd> <dl> <dt>



指定是否可以將內部和外部呼叫轉送至不同的轉送位址。 只有在可以個別控制內部和外部呼叫的轉送時，此旗標才有意義。 如果內部和外部呼叫可以轉送至不同的目的地位址，則此旗標為 **TRUE** ;否則為 **FALSE**。


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_FWDNUMRINGS"></span><span id="lineaddrcapflags_fwdnumrings"></span>**LINEADDRCAPFLAGS \_ FWDNUMRINGS**
</dt> <dd> <dl> <dt>



指定當轉送呼叫未接聽時，是否可指定無回應的環形數目。 若 **為 TRUE**，則會在 [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)結構的 **dwMinFwdNumRings** 和 **dwMaxFwdNumRings** 成員中提供有效的範圍。


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_FWDSTATUSVALID"></span><span id="lineaddrcapflags_fwdstatusvalid"></span>**LINEADDRCAPFLAGS \_ FWDSTATUSVALID**
</dt> <dd> <dl> <dt>



指定此位址的 [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) 結構中的轉送狀態是有效的，或最多為「最佳的估計值」，指出交換器或網路沒有正確的確認。


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_HOLDMAKESNEW"></span><span id="lineaddrcapflags_holdmakesnew"></span>**LINEADDRCAPFLAGS \_ HOLDMAKESNEW**
</dt> <dd> <dl> <dt>



使用 [**lineHold**](/windows/desktop/api/Tapi/nf-tapi-linehold) 或外部動作) 將此位址上的呼叫放置在保存 (時，會自動建立新的呼叫 (最有可能在 LINECALLSTATE 的 \_ 撥號程式) 。


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_NOEXTERNALCALLS"></span><span id="lineaddrcapflags_noexternalcalls"></span>**LINEADDRCAPFLAGS \_ NOEXTERNALCALLS**
</dt> <dd> <dl> <dt>



位址會與 PBX 上的內部線路相關聯，而這種方式不能用來對交換器以外的位址進行呼叫， (例如，它是對講機) 。 應用程式可以使用此指示，協助使用者選取正確的呼叫外觀以用來進行呼叫。 當這個位關閉時，不一定會指出位址可以用來進行外部呼叫，因為服務提供者可能不是行類型的 cognizant。


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_NOINTERNALCALLS"></span><span id="lineaddrcapflags_nointernalcalls"></span>**LINEADDRCAPFLAGS \_ NOINTERNALCALLS**
</dt> <dd> <dl> <dt>



位址會與 (主幹) 的直接 CO 線相關聯，而且無法用來在 PBX 上進行內部呼叫。 應用程式可以使用此指示，協助使用者選取正確的呼叫外觀以用來進行呼叫。 當這個位關閉時，不一定表示位址可以用來進行內部呼叫，因為服務提供者可能不是行類型的 cognizant。


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_NOPSTNADDRESSTRANSLATION"></span><span id="lineaddrcapflags_nopstnaddresstranslation"></span>**LINEADDRCAPFLAGS \_ NOPSTNADDRESSTRANSLATION**
</dt> <dd> <dl> <dt>



此位址不支援公用交換電話網路位址轉譯。 此旗標只會公開給協調 TAPI 3.0 版或更新版本的應用程式。


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_ORIGOFFHOOK"></span><span id="lineaddrcapflags_origoffhook"></span>**LINEADDRCAPFLAGS \_ ORIGOFFHOOK**
</dt> <dd> <dl> <dt>



指定進行呼叫時，是否可以自動 offhook 原始合作物件的電話。


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_PARTIALDIAL"></span><span id="lineaddrcapflags_partialdial"></span>**LINEADDRCAPFLAGS \_ PARTIALDIAL**
</dt> <dd> <dl> <dt>



指定是否可使用部分撥號。


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_PICKUPCALLWAIT"></span><span id="lineaddrcapflags_pickupcallwait"></span>**LINEADDRCAPFLAGS \_ PICKUPCALLWAIT**
</dt> <dd> <dl> <dt>



如果 [**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup)可以用來挑選使用者偵測到的呼叫做為呼叫等候呼叫，**則為 TRUE** 。否則 **為 FALSE**。


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_PICKUPGROUPID"></span><span id="lineaddrcapflags_pickupgroupid"></span>**LINEADDRCAPFLAGS \_ PICKUPGROUPID**
</dt> <dd> <dl> <dt>



指定呼叫取貨是否需要群組識別碼。


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_PREDICTIVEDIALER"></span><span id="lineaddrcapflags_predictivedialer"></span>**LINEADDRCAPFLAGS \_ PREDICTIVEDIALER**
</dt> <dd> <dl> <dt>



此位址具有增強的呼叫進度監視功能，可套用至連出呼叫以判斷撥號狀態（例如 *回電*、 *忙碌*、 *specialinfo* 和 *連線*），或接聽通話的裝置媒體類型。 它也可以在呼叫到達任何一組預先定義的狀態時，自動將撥出電話傳送到另一個位址。


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_QUEUE"></span><span id="lineaddrcapflags_queue"></span>**LINEADDRCAPFLAGS \_ 佇列**
</dt> <dd> <dl> <dt>



此位址不會與特定的工作站或實體裝置相關聯，而是呼叫等候進一步處理的位置。 放置在佇列中的呼叫可能會收到特定的處理。 當特定資源變成可用時，它們也可能會自動傳輸 (例如，如果佇列是 ACD 佇列，而呼叫正在等候可用的代理程式) 。


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_ROUTEPOINT"></span><span id="lineaddrcapflags_routepoint"></span>**LINEADDRCAPFLAGS \_ ROUTEPOINT**
</dt> <dd> <dl> <dt>



此位址不會與特定的工作站或實體裝置相關聯，而是由應用程式呼叫等候路由的位置， (應用程式會檢查呼叫的位址，並可將呼叫重新導向至另一個位址) 。 如果路由超時過期，則也會自動傳送呼叫 (切換通常會假設預設路由) 。


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_SECURE"></span><span id="lineaddrcapflags_secure"></span>**LINEADDRCAPFLAGS \_ 安全**
</dt> <dd> <dl> <dt>



指定是否可在呼叫設定時，將此位址上的呼叫設為安全。


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_SETCALLINGID"></span><span id="lineaddrcapflags_setcallingid"></span>**LINEADDRCAPFLAGS \_ SETCALLINGID**
</dt> <dd> <dl> <dt>



當呼叫 [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall)和其他接受 **LINECALLPARAMS** 結構的函式時，應用程式可以選擇在 [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams)中設定 **CallingPartyID** 成員。 如果識別碼的內容是可接受的，且有可用的路徑，服務提供者將會將識別碼傳遞給被呼叫的合作物件，以指出呼叫方的身分識別。


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_SETUPCONFNULL"></span><span id="lineaddrcapflags_setupconfnull"></span>**LINEADDRCAPFLAGS \_ SETUPCONFNull**
</dt> <dd> <dl> <dt>



指定是否要從初始呼叫開始設定會議通話 (**FALSE**) 或沒有初始呼叫 (**TRUE**) 。


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_TRANSFERHELD"></span><span id="lineaddrcapflags_transferheld"></span>**LINEADDRCAPFLAGS \_ TRANSFERHELD**
</dt> <dd> <dl> <dt>



指定是否可以傳送硬式通話。 通常，只有諮詢保留的呼叫可以轉移。


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_TRANSFERMAKE"></span><span id="lineaddrcapflags_transfermake"></span>**LINEADDRCAPFLAGS \_ TRANSFERMAKE**
</dt> <dd> <dl> <dt>



指定是否可以建立全新的呼叫，以作為傳輸時的諮詢通話。


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>備註

無延伸。 所有32位都是保留的。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 2.0 或更新版本<br/>                                             |
| 標頭<br/>       | <dl> <dt>Tapi</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**lineAccept**](/windows/desktop/api/Tapi/nf-tapi-lineaccept)
</dt> <dt>

[**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)
</dt> <dt>

[**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus)
</dt> <dt>

[**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams)
</dt> <dt>

[**lineCompleteCall**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall)
</dt> <dt>

[**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop)
</dt> <dt>

[**lineHold**](/windows/desktop/api/Tapi/nf-tapi-linehold)
</dt> <dt>

[**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall)
</dt> <dt>

[**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup)
</dt> </dl>

 

