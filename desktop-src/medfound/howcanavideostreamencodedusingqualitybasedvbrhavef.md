---
description: 使用以品質為基礎的 VBR 編碼的影片資料流程如何比原始串流更少的框架？
ms.assetid: acce9c88-2ee1-4628-9fd5-ccb441f8b43e
title: 使用以品質為基礎的 VBR 編碼的影片資料流程如何比原始串流更少的框架？
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad2af2775882155ed7ef2b0cfffdddeb30b2066e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192317"
---
# <a name="how-can-a-video-stream-encoded-using-quality-based-vbr-have-fewer-frames-than-the-original-stream"></a>使用以品質為基礎的 VBR 編碼的影片資料流程如何比原始串流更少的框架？

編碼資料流程的框架計數可以低於原始的框架計數，原因有兩種：重複的畫面格和已卸載的畫面格。

編碼器通常不會產生與前一個框架完全相同的畫面格。 如果您需要每個框架的範例 (這是某些容器所需的範例，例如) ，您可以將 [MFPKEY \_ PRODUCEDUMMYFRAMES](mfpkey-producedummyframesproperty.md) 屬性設定為 VARIANT TRUE，以將編碼器設定為產生「虛擬」畫面格 \_ 。

當編碼器無法編碼所有框架，而不會溢出緩衝區時，就會卸載框架。 捨棄的框架會影響資料流程的品質，而不會有重複的畫面格。

您可以從編碼器取得畫面格統計資料，以判斷是否已卸載框架。 如需詳細資訊，請參閱 [取得編碼統計資料](gettingencodingstatistics.md)。

通常，如果有重複的框架 (，以品質為基礎的 VBR 串流將只有較原始的框架較少，因為位元速率不受限制) 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[常見問題集](frequentlyaskedquestions.md)
</dt> </dl>

 

 



