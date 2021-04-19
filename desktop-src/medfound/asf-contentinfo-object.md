---
description: ASF ContentInfo 物件
ms.assetid: 6b7f8b68-fe98-4aeb-9842-a80ac6235999
title: ASF ContentInfo 物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bafa14279ab35c1c6986a8e19f302c764a587a97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106966657"
---
# <a name="asf-contentinfo-object"></a>ASF ContentInfo 物件

ASF *ContentInfo* 物件會儲存來自檔案之 ASF 標頭物件的資訊。 應用程式可基於下列目的使用 ContentInfo 物件：

-   讀取現有媒體檔案的標頭物件。 在此情況下，ContentInfo 物件會剖析標頭物件，並儲存特性檔案的相關資訊。 媒體基礎透過屬性和介面公開數個屬性。 這些會在 [ASF 標頭物件的媒體基礎屬性](media-foundation-attributes-for-asf-header-objects.md)中說明。
-   寫入標頭資訊，並為新檔案建立標頭物件。
-   在讀取或寫入媒體檔案時，初始化其他 ASF 物件，例如 [Asf 分隔器](asf-splitter.md)、 [Asf](asf-multiplexer.md)多工器和 asf 索引子。

如需 ASF 檔案結構的詳細資訊，請參閱 [asf 檔案結構](asf-file-structure.md)。

## <a name="creating-the-contentinfo-object"></a>建立 ContentInfo 物件

若要建立 ContentInfo 物件的新實例，請呼叫 [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) 函數。 這個方法會傳回空的 ContentInfo 物件的指標，此物件必須初始化以使用特定的 ASF 檔案。 根據應用程式是要讀取現有的檔案或寫入新的 ASF 檔案，它必須呼叫 [**IMFASFContentInfo：:P arseheader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) 或 [**IMFASFContentInfo：： SetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile) 來填入空的物件。

如需這些方法呼叫的詳細資訊，請參閱下列主題：

-   [讀取現有檔案的 ASF 標頭物件](reading-the-asf-header-object-of-an-existing-file.md)
-   [從 ASF 標頭物件取得資訊](getting-information-from-asf-header-objects.md)
-   [為新檔案撰寫 ASF 標頭物件](writing-an-asf-header-object-for-a-new-file.md)
-   [適用于 ASF 標頭物件的媒體基礎屬性](media-foundation-attributes-for-asf-header-objects.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[WMContainer ASF 元件](wmcontainer-asf-components.md)
</dt> </dl>

 

 



