---
description: DirectShow 濾波器開發簡介
ms.assetid: d5162ea4-ef37-4993-a82c-782f03b08c64
title: DirectShow 濾波器開發簡介
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2769cfe3bd4f046c117c0567104094bcad0eed730c388b551593dde6b41df25
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083688"
---
# <a name="introduction-to-directshow-filter-development"></a>DirectShow 濾波器開發簡介

本節提供有關開發自訂 DirectShow 篩選之工作的簡短大綱。 它也提供更詳細地討論這些工作的主題連結。 閱讀本節之前，請閱讀[有關 DirectShow](about-directshow.md)的主題，其中描述整體 DirectShow 架構。

**DirectShow基礎類別庫**

DirectShow SDK 包含一組用來寫入篩選器的 c + + 類別。 雖然它們並非必要，但建議您採用這些類別來撰寫新的篩選準則。 若要使用基類，請將它們編譯成靜態程式庫，並將 .lib 檔案連結至您的專案，如[建立 DirectShow 篩選器](building-directshow-filters.md)中所述。

基類庫會定義篩選的根類別，也就是 [**CBaseFilter**](cbasefilter.md) 類別。 有幾個其他類別衍生自 **CBaseFilter**，而且專屬於特定種類的篩選準則。 例如， [**CTransformFilter**](ctransformfilter.md) 類別是針對轉換篩選所設計。 若要建立新的篩選，請執行繼承自其中一個篩選準則類別的類別。 例如，您的類別宣告可能如下所示：


```C++
class CMyFilter : public CTransformFilter
{
private:
    /* Declare variables and methods that are specific to your filter.
public:
    /* Override various methods in CTransformFilter */
};
```



如需有關 DirectShow 基類的詳細資訊，請參閱下列主題：

-   [DirectShow基類](directshow-base-classes.md)
-   [建立 DirectShow 篩選](building-directshow-filters.md)

**建立釘選**

篩選準則必須建立一或多個 pin。 您可以在設計階段修正 pin 數目，或視需要建立新的釘選。 釘選通常衍生自 [**CBasePin**](cbasepin.md) 類別，或衍生自繼承 **CBasePin** 的類別，例如 [**CBaseInputPin**](cbaseinputpin.md)。 篩選器的 pin 應宣告為篩選準則類別中的成員變數。 某些篩選準則類別已定義釘選，但如果您的篩選準則直接繼承自 **CBaseFilter**，您就必須在衍生類別中宣告釘選。

**協商 Pin 連接**

當篩選 Graph 管理員嘗試連接兩個篩選器時，pin 必須同意各種不同的專案。 如果無法連線，連接嘗試就會失敗。 一般而言，pin 會協商下列各項：

-   傳輸。 傳輸是篩選器將用來將媒體樣本從輸出圖釘移至輸入釘選的機制。 例如，他們可以使用 [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) 介面 ( 「推送模型」 ) 或 [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) 介面 ( 「提取模型」 ) 。
-   媒體類型。 幾乎所有的針腳都會使用媒體類型來描述所要傳遞的資料格式。
-   分配器。 配置器是建立保存資料之緩衝區的物件。 Pin 必須同意哪些 pin 將提供配置器。 它們也必須同意緩衝區大小、要建立的緩衝區數目，以及其他緩衝區屬性。

基類會針對這些協商執行架構。 您必須覆寫基類中的各種方法，以完成詳細資料。 您必須覆寫的方法集合取決於類別以及篩選的功能。 如需詳細資訊，請參閱[連線的篩選準則](how-filters-connect.md)。

**處理和傳遞資料**

大部分篩選準則的主要功能是處理和傳遞媒體資料。 這種情況取決於篩選器的類型：

-   推送來源有一個背景工作執行緒，會持續以資料填滿範例，並將其傳遞至下游。
-   提取來源會等待其下游鄰近要求範例。 它會藉由將資料寫入範例，並將範例傳遞給下游篩選器來進行回應。 下游篩選器會建立驅動資料流程的執行緒。
-   轉換篩選具有其上游節點傳遞給它的範例。 當它收到範例時，它會處理資料並將它傳遞給下游。
-   轉譯器篩選器會從上游接收樣本，然後根據時間戳記進行排程以進行轉譯。

與串流相關的其他工作包括從圖形清除資料、處理資料流程的結尾，以及回應搜尋要求。 如需有關這些問題的詳細資訊，請參閱下列主題：

-   [篩選準則開發人員的資料 Flow](data-flow-for-filter-developers.md)
-   [品質控制管理](quality-control-management.md)
-   [執行緒和重要區段](threads-and-critical-sections.md)

**支援 COM**

DirectShow 篩選器是 COM 物件，通常封裝在 dll 中。 基類程式庫會實作為支援 COM 的架構。 如[DirectShow 和 COM](directshow-and-com.md)一節中所述。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[撰寫 DirectShow 篩選](writing-directshow-filters.md)
</dt> </dl>

 

 



