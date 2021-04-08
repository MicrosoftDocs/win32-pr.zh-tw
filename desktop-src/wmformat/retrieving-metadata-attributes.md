---
title: 正在抓取中繼資料屬性
description: 正在抓取中繼資料屬性
ms.assetid: d1d2c8e0-7445-4ee1-94d9-4c1ed74f8fe2
keywords:
- Windows Media Format SDK，正在抓取中繼資料屬性
- Advanced Systems Format (ASF) ，正在抓取中繼資料屬性
- ASF (Advanced Systems Format) ，正在抓取中繼資料屬性
- 中繼資料，正在抓取屬性
- 資料流程，正在抓取中繼資料屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c918cb47e77c3fd69c64de586b84b7f6244e4c9
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104023006"
---
# <a name="retrieving-metadata-attributes"></a>正在抓取中繼資料屬性

若要從檔案標頭取出屬性，您必須知道屬性的資料流程號碼和索引。 您可以使用 [**IWMHeaderInfo3：： GetAttributeIndices**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributeindices) 方法，以相同的語言取得具有相同名稱或所有索引的所有屬性的索引。 如同 [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3)的其他方法， **GetAttributeIndices** 會處理單一資料流程，或使用資料流程0來處理所有檔案層級的屬性。 您可以針對串流號碼使用0xFFFF，以取得符合整個檔案中的準則的全域索引（不論串流號碼為何）。

當您知道您想要取得之屬性的索引時，請呼叫 [**IWMHeaderInfo3：： GetAttributeByIndexEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributebyindexex) 來取得屬性。 您必須對每個抓取的屬性進行兩個 **GetAttributeByIndexEx** 呼叫。 在第一次呼叫時，傳遞 **Null** 作為名稱和資料緩衝區指標，以取得所需的大小。 然後，配置所指定大小的緩衝區，並進行第二次呼叫以取得名稱和資料。

如需示範如何取得中繼資料屬性的範例程式碼，請參閱 [取得檔案中的所有中繼資料](to-retrieve-all-metadata-in-a-file.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**使用中繼資料**](working-with-metadata.md)
</dt> </dl>

 

 




