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
# <a name="mftrace-configuration-file"></a>MFTrace 設定檔

[MFTrace](mftrace.md)工具可以讀取指定一個或多個追蹤提供者的 XML 設定檔。

[**Provider**](providers.md)元素是設定檔中的根項目。

## <a name="in-this-section"></a>本節內容

-   [**關鍵 字**](keyword.md)
-   [**mfdetours**](mfdetours.md)
-   [**供應商**](provider.md)
-   [**供應商**](providers.md)

## <a name="example"></a>範例

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

## <a name="related-topics"></a>相關主題

<dl> <dt>

[MFTrace](mftrace.md)
</dt> </dl>

 

 



