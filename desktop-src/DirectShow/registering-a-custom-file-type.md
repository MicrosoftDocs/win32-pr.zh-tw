---
description: 本文描述篩選圖形管理員如何找出檔案名，以尋找來源篩選。
ms.assetid: bc0d5719-6325-40fe-8261-ad00b91f272c
title: 註冊自訂檔案類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e98c01555497ac628fff452f464c826475edbb8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106970883"
---
# <a name="registering-a-custom-file-type"></a>註冊自訂檔案類型

本文描述篩選圖形管理員如何找出檔案名，以尋找來源篩選。 您可以使用此機制來註冊您自己的自訂檔案類型。 一旦註冊檔案類型，每當應用程式呼叫 [**IGraphBuilder：： RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) 或 [**IGraphBuilder：： AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter)時，DirectShow 都會自動載入正確的來源篩選器。

-   [概觀](#overview)
-   [通訊協定](#protocols)
-   [副檔名](#file-extensions)
-   [檢查位元組](#check-bytes)
-   [載入來源篩選](#loading-the-source-filter)
-   [Windows Media Player 中的自訂檔案類型](#custom-file-types-in-windows-media-player)
-   [相關主題](#related-topics)

## <a name="overview"></a>概觀

若要從指定的檔案名找出來源篩選，篩選圖形管理員會嘗試依序執行下列動作：

1.  符合通訊協定（如果有的話）。
2.  符合副檔名。
3.  符合檔案內的位元組模式，稱為 *檢查位元組*。

## <a name="protocols"></a>通訊協定

通訊協定名稱（例如 "ftp" 或 "HTTP"）會註冊在

**HKEY \_ 類別 \_ 根目錄**

具有下列結構的索引鍵：


```C++
HKEY_CLASSES_ROOT
    <protocol>
        Source Filter = <Source filter CLSID>
        Extensions
            <.ext1> = <Source filter CLSID>
            <.ext2> = <Source filter CLSID>
```



如果檔案名或 URL 包含冒號 ( '： ' ) ，則篩選圖形管理員會嘗試使用 '： ' 之前的部分做為通訊協定名稱。 例如，如果名稱為 "myprot://myfile.ext"，則會搜尋名為 **myprot** 的登錄機碼。 如果此索引鍵存在且包含名為 "Extensions" 的子機碼，則篩選圖形管理員會在該子機碼內搜尋符合副檔名的專案。 索引鍵的值必須是字串格式的 GUID。例如： " {00000000-0000-0000-0000-000000000000} "。 如果篩選圖形管理員無法比對 **延伸** 子機碼內的任何字元，則會尋找名為 **來源篩選** 器的子機碼，該子機碼必須也是字串格式的 GUID。

如果篩選圖形管理員找到相符的 GUID，則會使用此 GUID 做為來源篩選的 CLSID，並嘗試載入篩選。 如果找不到相符項，則會使用檔案 [來源 (url) ](file-source--url--filter.md) 篩選，這會將檔案名視為 url。

此演算法有兩種例外狀況：

-   若要排除驅動程式字母，則不會將單一字元字串視為通訊協定。
-   如果字串為 "file：" 或 "file://"，則不會將它視為通訊協定。

## <a name="file-extensions"></a>副檔名

如果檔案名中沒有通訊協定，則篩選圖形管理員會在登錄中尋找具有 key **HKEY \_ 類別 \_ 根 \\ 媒體類型 \\ 副檔名 \\** 的專案。*ext* \\ ，其中。*ext* 是副檔名。 如果此索引鍵存在，值 **來源篩選** 就會包含來源篩選的 CLSID （以字串形式）。 （選擇性）索引鍵可以有 **媒體類型** 和 **子** 類型的值，以提供主要類型和子類型 guid。

## <a name="check-bytes"></a>檢查位元組

某些檔案類型可透過在檔案中特定位元組位移處發生的特定位模式來識別。 篩選圖形管理員會在登錄中尋找下列格式的索引鍵：

**HKEY \_類別 \_ 根 \\ 媒體 \\***類型 {主要類型*} \\ {*子類型*}

其中的 *主要類型* 和 *子類型* 為 guid，可定義位元組資料流程的媒體類型。 每個金鑰都包含一或多個子機碼，通常名為1、2等等，以定義檢查位元組;和名為 **來源篩選器** 的子機碼，以字串形式提供來源篩選器的 CLSID。 檢查位元組子機碼是包含一或多個數位四邊形的字串，稱為：

*offset*、 *cb*、 *mask*、 *val*

為了比對檔案，篩選圖形管理員會讀取 cb 個位元組，從位元組數位移開始。 然後，它會對 mask 中的值執行位 AND。 如果結果等於 val，檔案就會符合該四個。 值 mask 和 val 會以十六進位提供。 遮罩的空白專案會視為長度為 cb 的1：1的字串。 Offset 的負數值表示從檔案結尾算出的位移。 為了符合此索引鍵，檔案必須符合任何子機碼中的所有四邊形。

例如，假設登錄在 **HKCR \\ 媒體類型** 下包含下列機碼：


```C++
{e436eb83-524f-11ce-9f53-0020af0ba770}
    {7364696D-0000-0010-8000-00AA00389B71}
        0                    "0,4,,52494646,8,4,,524D4944"
        1                    "0,4,,4D546864"
        Source Filter        "{E436EBB5-524F-11CE-9F53-0020AF0BA770}"
```



第一個索引鍵對應至主要型別媒體型 \_ 資料流程。 下面的子機碼會對應到類型為的型別（ \_ Midi）。 來源篩選子機碼的值是 CLSID \_ AsyncReader、檔案來源的 clsid [ (Async) ](file-source--async--filter.md) 篩選。

每個專案都可以有多個時;所有專案都必須相符。 在下列範例中，檔案的前4個位元組必須是0xAB、0xCD、0x12、0x34;而且檔案的最後4個位元組必須是0xAB、0xAB、0x00、0xAB：


```C++
    0, 4, , ABCD1234,  -4, 4, , ABAB00AB 
```



此外，單一媒體類型下可能會有多個專案。 其中任何一項都已足夠。 此配置允許一組替代的遮罩;例如，可能或可能不具有 RIFF 標頭的 .wav 檔。

> [!Note]  
> 此配置類似于 [**GetClassFile**](/windows/win32/api/objbase/nf-objbase-getclassfile) 函數所使用的配置。

 

## <a name="loading-the-source-filter"></a>載入來源篩選

假設篩選圖形管理員找到相符的檔案來源篩選器，它會將該篩選新增至圖形、查詢 [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter) 介面的篩選，以及呼叫 [**IFileSourceFilter：： Load**](/windows/desktop/api/Strmif/nf-strmif-ifilesourcefilter-load)。 **載入** 方法的引數是從登錄所決定的檔案名和媒體類型。

如果篩選圖形管理員在登錄中找不到任何檔案，則會預設為使用非同步檔案來源篩選。 在這種情況下，它會將媒體類型 **設定為媒體 \_** 類型， **MEDIASUBTYPE \_ 無**。

## <a name="custom-file-types-in-windows-media-player"></a>Windows Media Player 中的自訂檔案類型

Windows Media Player 會使用一組額外的登錄專案。 如需詳細資訊，請參閱 Windows Media Player SDK 中的 [副檔名登錄設定](../wmp/file-name-extension-registry-settings.md) 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[撰寫 DirectShow 篩選器](writing-directshow-filters.md)
</dt> </dl>

 

 
