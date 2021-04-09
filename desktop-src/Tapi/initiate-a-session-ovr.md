---
description: 應用程式提供來起始通訊會話的主要資訊片段包括網址類別型、媒體類型或類型，以及目的地位址。
ms.assetid: 65e53587-0e40-411b-8d6c-d6adfc9d1e6c
title: 起始會話
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e925ba90460b88c85a9aab1624923acdbc4572a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848660"
---
# <a name="initiate-a-session"></a>起始會話

應用程式提供來起始通訊會話的主要資訊片段包括 [網址類別型](address-type-ovr.md)、 [媒體類型](media-type-ovr.md) 或類型，以及目的地 [位址](address-ovr.md)。

目的地位址可能需要 [位址轉譯](#address-translation) ，才能將使用者輸入的資訊放入指定網址類別型的適當格式。 例如，位於 [標準](address-ovr.md) 格式電子通訊錄中的電話號碼，將需要翻譯成可 [撥](address-ovr.md) 出的格式。

某些會話可能需要特殊的安裝參數（如果服務提供者支援的話）。 例如，ISDN TSP 可以傳輸使用者的資訊，而某些 Msp 需要媒體資料流程方向的相關資訊。 請參閱 [會話資訊](session-information-ovr.md) ，以取得可針對會話設定或取得之資料的評論。

一旦啟動會話之後，TAPI 會使用初始化期間設定的事件通知機制，通知應用程式呼叫進度。

**TAPI 2.x：** 應用程式會使用 [**lineMakeCall**](/windows/win32/api/tapi/nf-tapi-linemakecall) 函式來初始化會話。 [**LineTranslateAddress**](/windows/win32/api/tapi/nf-tapi-linetranslateaddress)函式可用來執行位址轉譯（如有需要）。

呼叫安裝程式參數可以儲存在 [**LINECALLPARAMS**](/windows/win32/api/tapi/ns-tapi-linecallparams) 資料結構中，然後將此結構的指標當做 [**lineMakeCall**](/windows/win32/api/tapi/nf-tapi-linemakecall)的參數使用。 如果未提供 **LINECALLPARAMS** 結構給 **lineMakeCall**，則會以一組預設值要求預設的 POTS 語音等級通話。

如果會話已成功設定，則會將具有擁有者 [許可權](privilege-ovr.md)的呼叫控制碼傳回給應用程式，而 TAPI 會傳送應用程式 [**行 \_ CALLSTATE**](./line-callstate.md)訊息，其中包含有關呼叫進度的資訊。 應用程式通常會使用這些訊息來顯示狀態報表給使用者。

**TAPI 3.x：** 應用程式會叫用 [**ITAddress：： CreateCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-createcall) 方法，在能夠處理所需的網址類別型和媒體類型的位址上叫用通訊會話。 如果位址公開 [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport) 介面，則會在呼叫物件的媒體資料流程上選取終端機。 如需此程式的圖例，請參閱「 [提出通話](make-a-call.md) 程式碼」範例。

呼叫安裝程式參數可以使用 [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo) 介面所公開的方法來儲存或變更。

如果成功設定會話，TAPI 會傳回 [**ITBasicCallControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol) 介面指標，以供進一步的會話作業使用，或取得可用來取得其他會話資訊的 [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo) 介面指標。 [**ITCallStateEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallstateevent)介面會處理 TAPI 通話狀態事件。

> [!Note]  
> TAPI 不應用於傳真傳輸。 相反地，請使用可透過 MAPI 取得的函式，Microsoft 訊息中心 API。

 

## <a name="address-translation"></a>位址轉譯

使用者或伺服器應用程式可能會使用與指定服務提供者的需求不相容的格式來儲存位址。 例如，電話號碼可能會以 [標準格式](address-ovr.md)儲存在電子通訊錄中，但處理電話號碼的大部分服務提供者都需要可 [撥打的格式](address-ovr.md)。

TAPI 提供位址轉譯作業，可協助應用程式向 TSP 呈現正確的網址類別型。 服務提供者會指定 TAPI 所支援的網址類別型，而且不需要包含任何形式的位址轉譯。

**TAPI 2.x：** 請參閱 [**lineTranslateAddress**](/windows/win32/api/tapi/nf-tapi-linetranslateaddress)。

**TAPI 3：** 請參閱 [**ITAddressTranslation**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresstranslation)、 [**ITAddressTranslationInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresstranslationinfo)。

## <a name="toll-lists"></a>收費清單

在北美洲的某些位置中，放到本地區域程式碼的所有電話都是本機電話。 在其他位置中，放到區域程式碼的某些呼叫是很長的距離，而且需要撥出 "1" 前置詞。 位址 (前置詞的前三位數) 判斷局域程式碼中的呼叫是否為收費電話。

*收費清單* 是區域程式碼中的前置詞清單，其位址必須以長途電話位址的形式撥接，並經過評估的長途電話費用。

收費清單與服務提供者或未存取電話網絡的應用程式無關。

**TAPI 2.x：** 請 [](/windows/win32/api/tapi/nf-tapi-linetranslateaddress)參閱 \_ NOTINTOLLLIST 結構中的 lineTranslateAddress (LINETRANSLATERESULT INTOLLLIST 和 LINETRANSLATERESULT \_ LINETRANSLATEOUTPUT 位) ， [**lineSetTollList**](/windows/win32/api/tapi/nf-tapi-linesettolllist)。 [](/windows/win32/api/tapi/ns-tapi-linetranslateoutput)

**TAPI 3：** 請參閱 [**ITAddressTranslation：： TranslateAddress**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddresstranslation-translateaddress)， [**ITAddressTranslationInfo：： get \_ TranslationResults**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddresstranslationinfo-get_translationresults)。

 

 
