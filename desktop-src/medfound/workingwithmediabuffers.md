---
description: 使用 DMO 媒體緩衝區
ms.assetid: 6d0c51b8-0d79-4f04-8e90-0cea4f3b1427
title: 使用 DMO 媒體緩衝區
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 311778898fbfa669a602cd189fb5518f7a2814089a87ed33fba7e303c4327cac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118236954"
---
# <a name="working-with-dmo-media-buffers"></a>使用 DMO 媒體緩衝區

輸入資料會使用媒體緩衝區傳遞給編解碼器 DMOs。 媒體緩衝區是實 [**IMediaBuffer**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediabuffer) 介面的物件。 您可以針對此用途來執行類別，或者，如果您在應用程式中使用 Windows 媒體格式 SDK，則可以使用該 sdk 中定義的緩衝區物件。

如果您要執行自己的緩衝區類別，請小心處理緩衝區記憶體的處理方式。 當您傳遞輸入範例時，DMO 會保留緩衝區的參考，直到該範例完成為止。 您可以立即釋出 [**IMediaBuffer**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediabuffer) 介面的參考，但無法知道編解碼器不再需要它的參考。 若要確定當物件刪除時，記憶體會釋出，您應該執行類別，使其在內部為緩衝區配置和釋放記憶體。

由於 DMOs 會在未知的期間內保留緩衝區的參考，因此使用有限的緩衝區集區並不是很簡單的事。 最簡單的解決方案是為每個範例配置新的緩衝區，雖然這樣做沒有效率。

更好的解決方法是執行物件來管理緩衝區集區。 若要這樣做，請在 [**IMediaBuffer**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediabuffer)執行的 **Release** 方法中撰寫程式碼，以呼叫緩衝區管理員的方法， (而不是在參考計數降至零時刪除本身) 。 然後，緩衝區管理員可以維護已配置之緩衝區物件的指標清單。 在您的緩衝區管理員中建立方法，以檢查可用緩衝區清單並傳回指標，讓您的應用程式可以視需要存取緩衝區。 此方法應該視需要建立新的緩衝區，並將其新增至清單。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用編解碼器 DMOs](workingwithcodecdmos.md)
</dt> </dl>

 

 
