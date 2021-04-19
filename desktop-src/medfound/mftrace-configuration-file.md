---
description: MFTrace 工具可以讀取指定一個或多個追蹤提供者的 XML 設定檔。
ms.assetid: 70d11a55-041e-4eb5-96a9-238e7ecdd906
title: MFTrace 設定檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6598bcfdde16291fb744783b2f12be414ae997b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106991846"
---
# <a name="mftrace-configuration-file"></a><span data-ttu-id="3033a-103">MFTrace 設定檔</span><span class="sxs-lookup"><span data-stu-id="3033a-103">MFTrace Configuration File</span></span>

<span data-ttu-id="3033a-104">[MFTrace](mftrace.md)工具可以讀取指定一個或多個追蹤提供者的 XML 設定檔。</span><span class="sxs-lookup"><span data-stu-id="3033a-104">The [MFTrace](mftrace.md) tool can read an XML configuration file that specifies one or more trace providers.</span></span>

<span data-ttu-id="3033a-105">[**Provider**](providers.md)元素是設定檔中的根項目。</span><span class="sxs-lookup"><span data-stu-id="3033a-105">The [**providers**](providers.md) element is the root element in the configuration file.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="3033a-106">本節內容</span><span class="sxs-lookup"><span data-stu-id="3033a-106">In this section</span></span>

-   [<span data-ttu-id="3033a-107">**關鍵 字**</span><span class="sxs-lookup"><span data-stu-id="3033a-107">**keyword**</span></span>](keyword.md)
-   [<span data-ttu-id="3033a-108">**mfdetours**</span><span class="sxs-lookup"><span data-stu-id="3033a-108">**mfdetours**</span></span>](mfdetours.md)
-   [<span data-ttu-id="3033a-109">**供應商**</span><span class="sxs-lookup"><span data-stu-id="3033a-109">**provider**</span></span>](provider.md)
-   [<span data-ttu-id="3033a-110">**供應商**</span><span class="sxs-lookup"><span data-stu-id="3033a-110">**providers**</span></span>](providers.md)

## <a name="example"></a><span data-ttu-id="3033a-111">範例</span><span class="sxs-lookup"><span data-stu-id="3033a-111">Example</span></span>

``` syntax
<?xml version='1.0' encoding='utf-8'?>
<providers>
  <mfdetours level="info"> 
    <keyword ID="MFPlatExport" />
  </mfdetours>
  
  <!-- Manifest-based traces -->

  <provider level="verbose" ID="Microsoft-Windows-MediaFoundation-MFReadWrite">
    <keyword ID="0x0000000000000000" />
  </provider>

</providers>
```

## <a name="related-topics"></a><span data-ttu-id="3033a-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="3033a-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3033a-113">MFTrace</span><span class="sxs-lookup"><span data-stu-id="3033a-113">MFTrace</span></span>](mftrace.md)
</dt> </dl>

 

 



