---
description: 撥號作業可讓應用程式在先前建立的會話上傳送額外的數位。 部分撥號的使用範例是撥打延伸模組。 部分撥號有時稱為「增量撥號」或「延遲撥號」。
ms.assetid: 1dfaefd7-f8dd-451e-af18-249c89bdb517
title: 撥號
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1c603d8e846694b4728d1b5ad4c887be34fbac7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690067"
---
# <a name="dial"></a>撥號

撥號作業可讓應用程式在先前建立的會話上傳送額外的數位。 部分撥號的使用範例是撥打延伸模組。 部分撥號有時稱為「增量撥號」或「延遲撥號」。

當提供的位址未完成時，可能會藉由將分號 ( 來撥接部分數位，) 在數位的結尾。 接著會使用撥號操作，在現有的會話上傳送額外的位址資料，例如撥打將傳送呼叫的合作物件位址。

每個服務提供者都應該拒絕包含的撥號字串 **？** 字元，並讓應用程式適當地處理它。 例如，應用程式可以使用部分撥號來撥號字串，最多（但不包括） **？** 字元，然後顯示對話方塊，讓使用者在撥接其他的撥號字串時發出信號。

如果服務提供者不支援一或多個呼叫進度偵測控制字元，則應用程式使用部分撥號的另一個原因是該服務提供者。 這些字元可能發生在可撥撥的位址，是 W (等候撥號音) ;@ (等候無訊息回應) ;和 $ (等候電話卡提示語氣) 。 位址字串中使用的這些字元和其他所有字元，會在可 [撥](address-ovr.md)入的位址中更詳細地討論。

提供者會指出它所支援的「等候」撥號字串修飾詞。 TAPI 2 應用程式會在 [**lineGetDevCaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps)所傳回之 [**LINEDEVCAPS**](/windows/win32/api/tapi/ns-tapi-linedevcaps)結構的 **dwDevCapFlags** 成員中尋找這項資料。 TAPI 3 應用程式會呼叫 [**ITAddressCapabilities：： \_ get AddressCapability**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddresscapabilities-get_addresscapability) ，並將 *AddressCap* 設定為 [**ADDRESS \_ 功能**](/windows/desktop/api/Tapi3if/ne-tapi3if-address_capability)的 **AC \_ DEVCAPFLAGS** 成員。

應用程式可以選擇針對不支援的字元 prescan.exe 可撥打的字串，或者可以在起始會話的過程中傳遞「原始」字串。 如果字串包含不受支援的修飾詞或 "？"，則提供者會傳回錯誤，指出在字串中第一個發生的違規修飾詞：

-   LINEERR \_ DIALBILLING
-   LINEERR \_ DIALQUIET
-   LINEERR \_ DIALDIALTONE
-   LINEERR \_ DIALPROMPT

然後，應用程式可以在字串中找出違規的修飾詞、取得修飾詞左邊的數位、附加分號，然後使用部分位址初始化會話。 您可以使用撥號操作來傳送字串的其餘部分。

並非所有服務提供者都支援使用這項作業。

**TAPI 2.x：** 請參閱 [**lineDial**](/windows/win32/api/tapi/nf-tapi-linedial)。

**TAPI 3.x：** 請參閱 [**ITBasicCallControl：:D ial**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-dial)。

 

 
