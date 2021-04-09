---
description: 特定 Windows 媒體編碼器和管線層媒體基礎支援兩種編碼模式。
ms.assetid: 3fd5baff-142f-453e-bb97-b355ee6678fc
title: 如何建立 Two-Pass Windows Media 編碼的拓撲
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c813b9a3c31fafaa3efbea83180c997bc46079d
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "103945631"
---
# <a name="how-to-create-a-topology-for-two-pass-windows-media-encoding"></a>如何建立 Two-Pass Windows Media 編碼的拓撲

特定 Windows 媒體編碼器和管線層媒體基礎支援兩種編碼模式。 應用程式必須設定和設定類似于單一傳遞編碼方式的編碼拓撲，但在雙通路編碼模式中，應用程式必須執行編碼會話兩次。 在第一次通過時，編碼器會收集有關串流內容的資訊。 在第二個階段，藉由使用第一次傳遞時所收集的資訊，會產生最終的輸出檔。 藉由處理資料流程的範例兩次，兩次傳遞編碼會將編碼程式優化，並產生更高品質的編碼檔案。 無法在即時資料流上使用雙向編碼模式。

媒體基礎支援下列兩個傳遞的編碼模式：

-   [不受限制的變數位速率編碼](unconstrained-variable-bit-rate--vbr--encoding.md)
-   [尖峰限制的可變位速率編碼](peak-constrained-variable-bit-rate--vbr--encoding.md)

建立雙通路編碼的編碼拓撲類似于單一傳遞模式。 下列清單顯示主要的差異。

-   編碼器設定必須包含設定為2的 [**MFPKEY \_ PASSESUSED**](mfpkey-passesusedproperty.md) 屬性，以及 [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md) 屬性設為 VARIANT \_ TRUE。 這會將編碼器的功能篩選為雙通路模式。 如果您使用的是啟用物件，請將這些屬性傳遞至 [**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) 或 [**MFCreateWMVEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmvencoderactivate)。
-   針對第一次傳遞，請在輸出節點中使用虛擬媒體接收，因為在此階段中產生的範例不會加入至最終檔案。
-   針對第二個階段，查詢編碼器中是否有必要的編碼後內容，並以設定這些屬性的 ASF 媒體接收器取代 [虛擬媒體接收] 節點。

如需設定編碼拓撲的詳細資訊，請參閱 [教學課程：單一傳遞 Windows Media 編碼](tutorial--1-pass-windows-media-encoding.md)。

下列程式摘要說明在 ASF 容器中使用雙向編碼模式來編碼 Windows Media 內容的步驟。

1.  使用來源解析程式建立所指定的媒體來源。
2.  列舉媒體來源中的串流。
3.  根據媒體來源中需要編碼的資料流程，建立 ASF 媒體接收器並新增資料流程接收器。
4.  建立媒體接收器。
5.  在輸出檔中建立資料流程的 Windows Media 編碼器。
6.  使用2傳遞編碼屬性來設定編碼器。
7.  藉由連接來源、編碼器和媒體接收器來建立部分編碼拓撲。
8.  將媒體會話具現化，並在媒體會話上設定拓撲。
9.  藉由控制媒體會話並從媒體會話取得所有相關事件，來執行第一個編碼階段。
10. 關閉並關閉編碼會話。
11. 根據編碼類型，查詢編碼器中的下列屬性： 

    | 編碼類型                                                                                        | 屬性名稱                                                                                                                                                                                                                                                                                                                                                     |
    |------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | [不受限制的變數位速率編碼](unconstrained-variable-bit-rate--vbr--encoding.md)       | [**MFPKEY \_ PASSESUSED**](mfpkey-passesusedproperty.md)<br/> [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md)<br/> [**MFPKEY \_ BAVG**](mfpkey-bavgproperty.md)<br/> [**MFPKEY \_ RAVG**](mfpkey-ravgproperty.md)<br/>                                                                                                               |
    | [尖峰限制的可變位速率編碼](peak-constrained-variable-bit-rate--vbr--encoding.md) | [**MFPKEY \_ PASSESUSED**](mfpkey-passesusedproperty.md)<br/> [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md)<br/> [**MFPKEY \_ BAVG**](mfpkey-bavgproperty.md)<br/> [**MFPKEY \_ RAVG**](mfpkey-ravgproperty.md)<br/> [**MFPKEY \_ BMAX**](mfpkey-bmaxproperty.md)<br/> [**MFPKEY \_ RMAX**](mfpkey-rmaxproperty.md)<br/> |

    

     

12. 根據您想要包含在最終輸出檔中的資料流程，建立 ASF 檔案接收並新增必要的資料流程接收。
13. 在步驟11中，設定在檔接收器上抓取的編碼器屬性。
14. 將輸出節點中的媒體接收器取代為新建立的檔案接收。
15. 將媒體會話具現化，並在媒體會話上設定更新的拓撲。
16. 藉由控制媒體會話並從媒體會話取得所有相關事件，來執行第二次編碼階段。
17. 等候來自媒體會話的 [MEEndOfPresentation](meendofpresentation.md) 事件，然後在事件處理常式中取得編碼器的編碼屬性值，並在檔案接收上進行設定。 如需詳細資訊，請參閱 [教學課程：單一傳遞 Windows Media 編碼](tutorial--1-pass-windows-media-encoding.md)中的「更新 File 接收器中的編碼屬性」。
18. 關閉並關閉編碼會話。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[管線層 ASF 元件](pipeline-layer-asf-components.md)
</dt> </dl>

 

 




