---
title: '交易管理 (資料交換) '
description: 本主題討論用戶端如何傳送交易，以從伺服器取得資料和服務。
ms.assetid: 2d08ffa3-cbd7-4806-b94f-979938322c38
keywords:
- 'Windows 消費者介面，動態資料交換 (DDE) '
- 動態資料交換 (DDE) ，交易
- DDE (動態資料交換) ，交易
- '資料交換、動態資料交換 (DDE) '
- 'Windows 消費者介面、動態資料交換管理程式庫 (DDEML) '
- 動態資料交換管理程式庫 (DDEML) ，交易
- DDEML (動態資料交換管理程式庫) ，交易
- '資料交換、動態資料交換管理程式庫 (DDEML) '
- 動態資料交換 (DDE) ，要求交易
- DDE (動態資料交換) ，要求交易
- 動態資料交換管理程式庫 (DDEML) ，要求交易
- DDEML (動態資料交換管理程式庫) ，要求交易
- 動態資料交換 (DDE) ，請進行交易
- DDE (動態資料交換) ，進行交易
- 動態資料交換管理程式庫 (DDEML) ，請進行交易
- DDEML (動態資料交換管理程式庫) ，進行交易
- 動態資料交換 (DDE) ，建議交易
- DDE (動態資料交換) ，建議交易
- 動態資料交換管理程式庫 (DDEML) ，建議交易
- DDEML (動態資料交換管理程式庫) ，建議交易
- 動態資料交換 (DDE) ，執行交易
- DDE (動態資料交換) ，執行交易
- 動態資料交換管理程式庫 (DDEML) ，執行交易
- DDEML (動態資料交換管理程式庫) ，執行交易
- 動態資料交換 (DDE) ，同步交易
- DDE (動態資料交換) ，同步交易
- 動態資料交換管理程式庫 (DDEML) ，同步交易
- DDEML (動態資料交換管理程式庫) ，同步交易
- 動態資料交換 (DDE) 、非同步交易
- DDE (動態資料交換) 、非同步交易
- 動態資料交換管理程式庫 (DDEML) 、非同步交易
- DDEML (動態資料交換管理程式庫) 、非同步交易
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 570aa48b4dcdbb31855b3e1b15a091908feb2ba4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023617"
---
# <a name="transaction-management-data-exchange"></a>交易管理 (資料交換) 

建立與伺服器的對話之後，用戶端就可以傳送交易來取得伺服器的資料和服務。

下列主題描述用戶端可以用來與伺服器互動的交易類型。

-   [要求交易](#request-transaction)
-   [進行交易](#poke-transaction)
-   [建議交易](#advise-transaction)
-   [執行交易](#execute-transaction)
-   [同步和非同步交易](#synchronous-and-asynchronous-transactions)
-   [交易控制](#transaction-control)
-   [交易類別](#transaction-classes)
-   [交易類型](#transaction-types)

## <a name="request-transaction"></a>要求交易

用戶端應用程式可以使用 [**XTYP \_ 要求**](xtyp-request.md) 交易來要求伺服器應用程式中的資料項目。 用戶端會呼叫 [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) 函式，並將 **XTYP \_ 要求** 指定為交易類型並指定應用程式所需的資料項目。

動態資料交換管理程式庫 (DDEML) 會將 [**XTYP \_ 要求**](xtyp-request.md) 交易傳遞至伺服器，並指定用戶端所要求的主題名稱、專案名稱和資料格式。 如果伺服器支援要求的主題、專案及格式，伺服器應該會傳回識別專案目前值的資料控制碼。 DDEML 會將這個控制碼傳遞給用戶端，做為 [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)的傳回值。 如果伺服器不支援所要求的主題、專案或格式，則應該傳回 **Null** 。

[**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) 使用 *lpdwResult* 參數將交易狀態旗標傳回至用戶端。 如果伺服器未處理 [**XTYP \_ 要求**](xtyp-request.md) 交易， **DdeClientTransaction** 會傳回 **Null**，而 *lpdwResult* 會指向 dde \_ FNOTPROCESSED 或 dde \_ FBUSY 旗標。 如果傳回了 DDE \_ FNOTPROCESSED 旗標，用戶端就無法判斷伺服器為何無法處理交易。

如果伺服器不支援 [**XTYP \_ 要求**](xtyp-request.md)交易，則應該在 DdeInitialize 函式中指定 CBF \_ 失敗 \_ 要求篩選旗標 [](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) 。 此旗標會防止 DDEML 將交易傳送到伺服器。

## <a name="poke-transaction"></a>進行交易

用戶端可以使用 [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) 將未經要求的資料傳送到伺服器，以 [**將 \_ XTYP**](xtyp-poke.md) 的郵件傳送到伺服器的回呼函數。

用戶端應用程式會先建立一個緩衝區，其中包含要傳送至伺服器的資料，然後將緩衝區的指標以參數形式傳遞至 [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)。 或者，用戶端可以使用 [**DdeCreateDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle) 函數來取得可識別資料的資料控制碼，然後將控制碼傳遞至 **DdeClientTransaction**。 無論是哪一種情況，用戶端也會在呼叫 **DdeClientTransaction** 時指定主題名稱、專案名稱和資料格式。

DDEML 會將 [**XTYP 的 \_**](xtyp-poke.md) 傳送交易傳遞給伺服器，並指定用戶端所要求的主題名稱、專案名稱和資料格式。 若要接受資料項目和格式，伺服器應該傳回 DDE \_ FACK。 若要拒絕資料，伺服器應該傳回 DDE \_ FNOTPROCESSED。 如果伺服器太忙碌而無法接受資料，伺服器應該會傳回 DDE \_ FBUSY。

當 [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) 傳回時，用戶端可以使用 *lpdwResult* 參數來存取交易狀態旗標。 如果旗標是 DDE \_ FBUSY，用戶端應該稍後再傳送交易。

如果伺服器不支援 XTYP 伺服器的 [**交易 \_**](xtyp-poke.md) ，則應該 \_ 在 DdeInitialize 中指定 CBF FAIL \_ 友善篩選旗標 [](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)。 此旗標會防止 DDEML 將此交易傳送到伺服器。

## <a name="advise-transaction"></a>建議交易

用戶端應用程式可以使用 DDEML，在伺服器應用程式中建立專案的一個或多個連結。 當您建立這類連結時，伺服器會定期將有關連結專案的更新傳送至用戶端 (一般而言，只要與伺服器應用程式相關聯的專案值變更) 。 連結會在兩個保留位置的應用程式之間建立一個建議迴圈，直到用戶端結束為止。

有兩種類型的建議迴圈：「經常性存取」和「熱」。 在熱建議迴圈中，伺服器會立即傳送可識別變更值的資料控制碼。 在暖建議迴圈中，伺服器會通知用戶端專案的值已變更，但在用戶端要求之前，不會傳送資料控制碼。

用戶端可以在對 [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)的呼叫中指定 [**XTYP \_ ADVSTART**](xtyp-advstart.md)交易類型，藉以向伺服器要求熱建議迴圈。 若要要求暖建議迴圈，用戶端必須結合 XTYPF \_ NODATA 旗標與 **XTYP \_ ADVSTART** 交易類型。 在任一事件中，DDEML 會將 **XTYP \_ ADVSTART** 交易傳遞給伺服器的動態資料交換 (DDE) 回呼函式。 伺服器的 DDE 回呼函數應該檢查 **XTYP \_ ADVSTART** transaction 伴隨的參數 (包括要求的格式、主題名稱和專案名稱) 然後傳回 **TRUE** 以允許建議迴圈或 **FALSE** 拒絕它。

在建立「建議」迴圈之後，每當與要求的專案名稱相關聯的專案值變更時，伺服器應用程式就應該呼叫 [**DdePostAdvise**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise) 函數。 這項呼叫會導致將 [**XTYP \_ ADVREQ**](xtyp-advreq.md) 交易傳送到伺服器本身的 DDE 回呼函數。 伺服器的 DDE 回呼函數應該會傳回識別資料項目新值的資料控制碼。 然後，DDEML 會將 [**XTYP \_ ADVDATA**](xtyp-advdata.md) 交易傳送至用戶端的 DDE 回呼函式，以通知用戶端指定的專案已經變更。

如果用戶端要求熱建議迴圈，DDEML 會在 [**XTYP \_ ADVDATA**](xtyp-advdata.md) 交易期間，將已變更的專案傳遞至用戶端。 否則，用戶端可以傳送 [**XTYP \_ 要求**](xtyp-request.md) 交易來取得資料控制碼。

伺服器可以更快地傳送更新，而不是用戶端可以處理新資料。 對於必須對資料執行冗長處理作業的用戶端而言，更新的速度可能會造成問題。 在此情況下，用戶端應該在要求「建議」迴圈時，指定 XTYPF \_ ACKREQ 旗標。 此旗標會讓伺服器在伺服器傳送下一個資料項目之前，等待用戶端確認它已接收並處理資料項目。 使用 XTYPF ACKREQ 旗標所建立的建議迴圈， \_ 會比快速伺服器更健全，但偶爾會遺漏更新。 \_只要用戶端跟上伺服器，就不會遺漏 XTYPF ACKREQ 旗標所建立的建議迴圈。

用戶端可以在對 [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)的呼叫中指定 [**XTYP \_ ADVSTOP**](xtyp-advstop.md)交易類型，藉以結束「建議」迴圈。

如果伺服器不支援「建議」迴圈，則應該在 DdeInitialize 函式中指定 CBF \_ 失敗 \_ 建議[](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)篩選旗標。 此旗標會防止 DDEML 將 [**XTYP \_ ADVSTART**](xtyp-advstart.md) 和 [**XTYP \_ ADVSTOP**](xtyp-advstop.md) 交易傳送到伺服器。

## <a name="execute-transaction"></a>執行交易

用戶端可以使用 [**XTYP \_ execute**](xtyp-execute.md) 交易，讓伺服器執行命令或一系列的命令。

若要執行伺服器命令，用戶端會先建立一個緩衝區，其中包含要執行之伺服器的命令字串，然後在呼叫 [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)時，將指標傳遞至緩衝區或識別緩衝區的資料控制碼。 其他必要參數包括交談控制碼、專案名稱字串控制碼、格式規格，以及 [**XTYP \_ 執行**](xtyp-execute.md) 交易類型。 建立資料處理程式以傳遞執行資料的應用程式，必須針對 [**DdeCreateDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle)函式的 *HszItem* 參數指定 **Null** ，並針對 *uFmt* 參數指定為零。

DDEML 會將 [**XTYP \_ 執行**](xtyp-execute.md) 交易傳遞給伺服器的 DDE 回呼函式，並指定用來識別命令字串的格式名稱、對話控制碼、主題名稱和資料控制碼。 如果伺服器支援命令，它應該使用 [**DdeAccessData**](/windows/desktop/api/Ddeml/nf-ddeml-ddeaccessdata) 函式來取得命令字串的指標，執行命令，然後傳回 DDE \_ FACK。 如果伺服器不支援命令或無法完成交易，它應該會傳回 DDE \_ FNOTPROCESSED。 \_如果伺服器太忙碌而無法完成交易，伺服器應該會傳回 DDE FBUSY。

一般來說，伺服器的回呼函數應該先處理 [**XTYP \_ EXECUTE**](xtyp-execute.md) 交易，然後再傳回，但有下列例外狀況：

1.  當使用 [**XTYP \_ EXECUTE**](xtyp-execute.md) transaction 傳遞的命令要求伺服器終止時，伺服器不應終止，直到其回呼函數從處理 **XTYP \_ 執行** 傳回為止。
2.  如果伺服器必須執行作業（例如處理對話方塊或可能造成 DDEML 遞迴問題的 DDE 交易），伺服器應該會傳回 CBR \_ 區塊傳回碼來封鎖執行交易、執行作業，然後繼續處理執行交易。

當 [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) 傳回時，用戶端可以使用 *lpdwResult* 參數來存取交易狀態旗標。 如果旗標是 DDE \_ FBUSY，用戶端應該稍後再傳送交易。

如果伺服器不支援 [**XTYP \_ EXECUTE**](xtyp-execute.md) transaction，則應該 \_ \_ 在 [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) 函數中指定 CBF FAIL EXECUTE filter 旗標。 這樣做可防止 DDEML 將交易傳送到伺服器。

## <a name="synchronous-and-asynchronous-transactions"></a>同步和非同步交易

用戶端可以傳送同步或非同步交易。 在同步交易中，用戶端會指定超時值，指出等候伺服器處理交易的最大時間量。 除非伺服器處理交易、交易失敗或超時值過期，否則 [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)不會傳回。 用戶端會在呼叫 **DdeClientTransaction** 時指定超時值。

在同步交易期間，用戶端會在等候交易處理時進入強制回應迴圈。 用戶端仍然可以處理使用者輸入，但在 [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) 傳回之前無法傳送另一個同步交易。

用戶端藉由 \_ 在 [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)中指定 TIMEOUT ASYNC 旗標來傳送非同步交易。 此函數會在交易開始之後傳回，並將交易識別碼傳遞給用戶端。 當伺服器完成非同步交易處理時，DDEML 會將 XTYP 的 [**交易 \_ \_ 完成**](xtyp-xact-complete.md) 交易傳送給用戶端。 DDEML 在 **XTYP 交易 \_ \_ 完成** 交易期間傳遞給用戶端的其中一個參數是交易識別碼。 藉由比較此交易識別碼與 **DdeClientTransaction** 所傳回的識別碼，用戶端會識別伺服器已完成處理的非同步交易。

用戶端可以使用 [**DdeSetUserHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddesetuserhandle) 函數來協助處理非同步交易。 此函數可讓用戶端將應用程式定義值與交談控制碼和交易識別碼產生關聯。 用戶端可以在 [**XTYP 交易 \_ \_ 完成**](xtyp-xact-complete.md)交易期間使用 [**DdeQueryConvInfo**](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo)函式，以取得應用程式定義的值。 由於這個函式的原因，應用程式不需要維護使用中交易識別碼的清單。

當用戶端使用同步交易成功完成資料的要求時，DDEML 無法分辨用戶端何時完成使用所收到的資料。 用戶端應用程式必須將接收到的資料控制碼傳遞至 [**DdeFreeDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddefreedatahandle) 函式，以通知 DDEML 該控制碼將不再使用。 同步交易所傳回的資料控制碼實際上是由用戶端所擁有。

如果伺服器沒有及時處理非同步交易，用戶端可以藉由呼叫 [**DdeAbandonTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeabandontransaction) 函數來放棄交易。 DDEML 會釋放與交易相關聯的所有資源，並在伺服器完成處理時捨棄交易結果。 同步交易期間的超時時間會有效地取消交易。

非同步交易方法是針對必須傳送大量 DDE 交易的應用程式所提供，同時執行大量的處理，例如執行計算。 非同步方法也適用于必須暫時停止處理 DDE 交易的應用程式，讓它們可以在不中斷的情況下完成其他工作。 在大部分的其他情況下，應用程式應該使用同步方法。

同步交易比較容易維護，而且速度比非同步交易更快。 不過，一次只能執行一個同步交易，而許多非同步交易則可以同時執行。 使用同步交易時，緩慢的伺服器可能會導致用戶端在等候回應時保持閒置。 此外，同步交易也會導致用戶端進入強制回應迴圈，該迴圈可能會略過應用程式本身訊息迴圈中的訊息篩選。

如果用戶端已安裝攔截程式來篩選訊息 (也就是在 SetWindowsHookEx 函式的呼叫中指定了 WH \_ MSGFILTER 攔截[](/windows/desktop/api/winuser/nf-winuser-setwindowshookexa)類型) ，同步交易將不會造成系統略過攔截程式。 當用戶端在等候同步交易結束時，如果發生輸入事件，攔截程式就會收到 MSGF DDEMGR 攔截程式 \_ 代碼。 使用同步交易強制回應迴圈的主要風險是，對話方塊所建立的強制回應迴圈可能會干擾其作業。 當 DLL 正在使用 DDEML 時，應該一律使用非同步交易。

## <a name="transaction-control"></a>交易控制

無論對話控制碼為何，應用程式都可以將交易暫停至其 DDE 回呼函式，這些交易與特定對話控制碼或所有交易相關聯。 當應用程式收到需要冗長處理的交易時，這項功能就很有用。 在這種情況下，應用程式可以傳回 CBR \_ 區塊傳回碼，以暫止與交易交談控制碼相關聯的未來交易，讓應用程式可以自由處理其他交談。

當處理完成時，應用程式會呼叫 [**DdeEnableCallback**](/windows/desktop/api/Ddeml/nf-ddeml-ddeenablecallback) 函數來繼續與已暫停交談相關聯的交易。 呼叫 **DdeEnableCallback** 會導致 DDEML 重新傳送導致應用程式暫停交談的交易。 因此，應用程式應該儲存交易的結果，讓它可以取得並傳回結果，而不需要重新處理交易。

應用程式可以藉由在 DdeEnableCallback 的呼叫中指定控制碼和 EC DISABLE 旗標，來暫停與特定對話控制碼相關聯的所有交易 \_ 。 [](/windows/desktop/api/Ddeml/nf-ddeml-ddeenablecallback) 藉由指定 **Null** 控制碼，應用程式可以暫止所有交談的所有交易。

當交談暫停時，DDEML 會將交談的交易儲存在交易佇列中。 當應用程式 reenables 交談時，DDEML 會從佇列中移除已儲存的交易，並將每個交易傳遞給適當的回呼函數。 交易佇列的容量很大，但應用程式應該儘快重新啟用暫停的交談，以避免遺失交易。

應用程式可以 \_ 在 [**DdeEnableCallback**](/windows/desktop/api/Ddeml/nf-ddeml-ddeenablecallback)中指定 EC ENABLEALL 旗標，以繼續正常交易處理。 針對更受控制的交易處理繼續，應用程式可以指定 EC \_ ENABLEONE 旗標。 此旗標會移除交易佇列中的一筆交易，並將其傳遞至適當的回呼函式;交易經過處理之後，就會再次停用任何交談。

如果在 \_ 呼叫 [**DdeEnableCallback**](/windows/desktop/api/Ddeml/nf-ddeml-ddeenablecallback)時指定了 EC ENABLEONE 旗標和交談控制碼，只有在處理交易之後，才會封鎖該交談。 如果指定了 **Null** 對話控制碼，則在任何交談中處理交易之後，會封鎖所有交談。

## <a name="transaction-classes"></a>交易類別

DDEML 有四個類別的交易。 每個類別都是由以 XCLASS 前置詞開頭的常數來識別 \_ 。 這些類別定義于 DDEML 標頭檔中。 類別值會與交易類型值結合，並傳遞至接收應用程式的 DDE 回呼函數。

交易的類別會決定回呼函數在處理交易時預期會傳回的傳回值。 下列傳回值和交易類型會與四個交易類別相關聯。



| 類別                | 傳回值                                                     | 交易                                                                                                                                                                                                                                                                                                                                                                                    |
|----------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| XCLASS \_ BOOL         | **TRUE** 或 **FALSE**                                            | [**XTYP \_ ADVSTART**](xtyp-advstart.md)<br/> [**XTYP \_ 連接**](xtyp-connect.md)<br/>                                                                                                                                                                                                                                                                                            |
| XCLASS \_ 資料         | 資料控制碼、CBR \_ 區塊傳回碼或 **Null**           | [**XTYP \_ ADVREQ**](xtyp-advreq.md)<br/> [**XTYP \_ 要求**](xtyp-request.md)<br/> [**XTYP \_ WILDCONNECT**](xtyp-wildconnect.md)<br/>                                                                                                                                                                                                                                       |
| XCLASS \_ 旗標        | 交易旗標： DDE \_ FACK、dde \_ FBUSY 或 dde \_ FNOTPROCESSED | [**XTYP \_ ADVDATA**](xtyp-advdata.md)<br/> [**XTYP \_ EXECUTE**](xtyp-execute.md)<br/> [**XTYP \_**](xtyp-poke.md)<br/>                                                                                                                                                                                                                                                   |
| XCLASS \_ 通知 | 無                                                             | [**XTYP \_ ADVSTOP**](xtyp-advstop.md)<br/> [**XTYP \_ CONNECT \_ 確認**](xtyp-connect-confirm.md)<br/> [**XTYP \_ 中斷連線**](xtyp-disconnect.md)<br/> [**XTYP \_ 錯誤**](xtyp-error.md)<br/> [**XTYP \_ 註冊**](xtyp-register.md)<br/> [**XTYP \_ 取消註冊**](xtyp-unregister.md)<br/> [**XTYP \_ 交易 \_ 完成**](xtyp-xact-complete.md)<br/> |



 

## <a name="transaction-types"></a>交易類型

每個 DDE 交易類型都有接收者和相關聯的活動，可讓 DDEML 產生每個型別。



| 交易類型                                       | 接收者                   | 原因                                                                                                                                                                         |
|--------------------------------------------------------|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**XTYP \_ ADVDATA**](xtyp-advdata.md)                  | 用戶端                     | 伺服器藉由傳回資料處理程式來回應 [**XTYP \_ ADVREQ**](xtyp-advreq.md) 交易。                                                                          |
| [**XTYP \_ ADVREQ**](xtyp-advreq.md)                    | 伺服器                     | 稱為 [**DdePostAdvise**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise) 函數的伺服器，指出建議迴圈中資料項目的值已變更。                                  |
| [**XTYP \_ ADVSTART**](xtyp-advstart.md)                | 伺服器                     | 用戶端在 [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)函數的呼叫中指定了 [**XTYP \_ ADVSTART**](xtyp-advstart.md)交易類型。               |
| [**XTYP \_ ADVSTOP**](xtyp-advstop.md)                  | 伺服器                     | 用戶端在對 [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)的呼叫中指定了 [**XTYP \_ ADVSTOP**](xtyp-advstop.md)交易類型。                              |
| [**XTYP \_ 連接**](xtyp-connect.md)                  | 伺服器                     | 稱為 [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) 函式的用戶端，並指定伺服器所支援的服務名稱和主題名稱。                                            |
| [**XTYP \_ CONNECT \_ 確認**](xtyp-connect-confirm.md) | 伺服器                     | 伺服器傳回 **TRUE** 以回應 [**XTYP \_ CONNECT**](xtyp-connect.md) 或 [**XTYP \_ WILDCONNECT**](xtyp-wildconnect.md) 交易。                            |
| [**XTYP \_ 中斷連線**](xtyp-disconnect.md)            | 用戶端/伺服器              | 交談中名為 [**DdeDisconnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnect) 函式的夥伴，會導致這兩個夥伴接收此交易。                                    |
| [**XTYP \_ 錯誤**](xtyp-error.md)                      | 用戶端/伺服器              | 發生嚴重錯誤。 DDEML 可能沒有足夠的資源可以繼續。                                                                                       |
| [**XTYP \_ EXECUTE**](xtyp-execute.md)                  | 伺服器                     | 用戶端在呼叫 [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)時指定了 [**XTYP \_ EXECUTE**](xtyp-execute.md)交易類型。                              |
| [**XTYP \_ 監視**](xtyp-monitor.md)                  | DDE 監視應用程式 | 系統中發生 DDE 事件。 如需有關 DDE 監視應用程式的詳細資訊，請參閱 [監視應用程式](monitoring-applications.md)。                       |
| [**XTYP \_**](xtyp-poke.md)                        | 伺服器                     | 用戶端在呼叫 [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)時，指定了 [**XTYP \_**](xtyp-poke.md)的處理類型。                                    |
| [**XTYP \_ 註冊**](xtyp-register.md)                | 用戶端/伺服器              | 伺服器應用程式使用 [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) 函數來註冊服務名稱。                                                                   |
| [**XTYP \_ 要求**](xtyp-request.md)                  | 伺服器                     | 用戶端在呼叫 [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)時指定了 [**XTYP \_ 要求**](xtyp-request.md)交易類型。                              |
| [**XTYP \_ 取消註冊**](xtyp-unregister.md)            | 用戶端/伺服器              | 使用 [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) 取消註冊服務名稱的伺服器應用程式。                                                                              |
| [**XTYP \_ WILDCONNECT**](xtyp-wildconnect.md)          | 伺服器                     | 稱為 [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) 或 [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) 函式的用戶端，針對服務名稱指定 **Null** 、主題名稱或兩者。 |
| [**XTYP \_ 交易 \_ 完成**](xtyp-xact-complete.md)     | 用戶端                     | 非同步交易（當用戶端在 \_ 呼叫 [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)的呼叫中指定 TIMEOUT ASYNC 旗標時傳送）已結束。         |



 

 

