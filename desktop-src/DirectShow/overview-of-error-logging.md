---
description: 錯誤記錄總覽
ms.assetid: 1037f354-0415-4a5c-a96c-20ae714981af
title: 錯誤記錄總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcde3e0366ffca12dfcb5674259273ba1bbf25c1feed9be3ead57fa64cc42dc4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119904628"
---
# <a name="overview-of-error-logging"></a>錯誤記錄總覽

\[此 API 不受支援，而且可能會在未來變更或無法使用。\]

為了讓應用程式在處理錯誤時擁有最大的彈性， [DirectShow 編輯服務](directshow-editing-services.md)會使用回呼機制。 您的應用程式會執行記錄錯誤的方法。 在執行時間，如果發生錯誤，DES 會呼叫您提供的方法。 方法會使用描述錯誤的參數。 使用此資訊的方法是由您決定。  (應該儘快傳回，否則可能會干擾程式的執行。 ) 

錯誤記錄回呼方法包含在 COM 介面 [**IAMErrorLog**](iamerrorlog.md)中。 您的應用程式必須執行這個介面。 如同所有的 COM 介面， **IAMErrorLog** 會繼承 **IUnknown** 介面，因此您的應用程式也必須執行該介面。

您有數個選項可執行這些 COM 介面。 您可以使用 Active Template Library (ATL) ，它會提供 **IUnknown** 方法的庫存實作為。 DirectShow 也提供 c + + 基類 [**CUnknown**](cunknown.md)，可讓您輕鬆地執行 COM 介面。 如需使用 **CUnknown** 的詳細資訊，請參閱 [如何執行 IUnknown](how-to-implement-iunknown.md)。

本文中的範例程式碼會定義獨立的 c + + 類別，以同時執行 **IUnknown** 和 **IAMErrorLog**。 結果不是真正的 COM 物件，因為它不支援 **CoCreateInstance**。 不過，這種方法適用于範例的目的。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[記錄錯誤](logging-errors.md)
</dt> </dl>

 

 



