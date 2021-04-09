---
description: 補充的電話語音服務是由 API 定義的所有服務的集合，而不是基本電話語音子集中包含的所有服務。
ms.assetid: a2a30a0d-fbfd-4317-8e3a-d1e1e8b86ae0
title: 補充電話語音服務
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d93a7d12840e2001c6a2742e6bbd870d291e836
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849227"
---
# <a name="supplementary-telephony-services"></a>補充電話語音服務

補充的電話語音服務是由 API 定義的所有服務的集合，而不是基本電話語音子集中包含的所有服務。 它包含在新式 Pbx 上找到的所有所謂的補充功能，例如保存、傳輸、會議、公園等等。 所有增補功能都會被視為選擇性;也就是說，服務提供者會決定其所執行或未提供的服務。

應用程式可以使用 [**lineGetDevCaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps) 或 [**lineGetAddressCaps**](/windows/win32/api/tapi/nf-tapi-linegetaddresscaps)等函式，為它所提供的一組補充服務查詢線路或電話裝置。 單一補充服務可能包含多個函式呼叫和訊息。 電話語音 API （而不是服務提供者開發人員）會定義每個補充功能的行為。 只有當服務提供者可以依照 API 所定義的確切意義來執行時，才會提供補充的電話語音服務。 如果沒有，則應以擴充電話語音服務的形式提供此功能。

如基本電話語音服務所述，手機裝置服務會視為選擇性。 因此，所有的電話裝置服務都是補充電話語音的一部分。 如需補充電話語音的功能清單，請參閱 [TAPI 快速功能參考](./tapi-quick-function-reference.md)。

 

 
