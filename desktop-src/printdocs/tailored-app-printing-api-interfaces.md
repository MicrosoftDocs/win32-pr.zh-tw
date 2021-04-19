---
description: 應用程式會使用下列介面來管理列印檔案套件。
ms.assetid: 576B4527-A753-4A73-899B-896DCB8B8945
title: 列印檔案套件 API 介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adc495be5c58598d00250568ff852cf4f897e0b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106992086"
---
# <a name="print-document-package-api-interfaces"></a><span data-ttu-id="33dd9-103">列印檔案套件 API 介面</span><span class="sxs-lookup"><span data-stu-id="33dd9-103">Print Document Package API Interfaces</span></span>

<span data-ttu-id="33dd9-104">應用程式會使用下列介面來管理列印檔案套件。</span><span class="sxs-lookup"><span data-stu-id="33dd9-104">The following interfaces are used by an app to manage the print document package.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="33dd9-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="33dd9-105">In this section</span></span>



| <span data-ttu-id="33dd9-106">主題</span><span class="sxs-lookup"><span data-stu-id="33dd9-106">Topic</span></span>                                                                                       | <span data-ttu-id="33dd9-107">描述</span><span class="sxs-lookup"><span data-stu-id="33dd9-107">Description</span></span>                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="33dd9-108">**IPrintDocumentPackageStatusEvent**</span><span class="sxs-lookup"><span data-stu-id="33dd9-108">**IPrintDocumentPackageStatusEvent**</span></span>](/windows/desktop/api/Documenttarget/nn-documenttarget-iprintdocumentpackagestatusevent)<br/>     | <span data-ttu-id="33dd9-109">代表列印工作的進度。</span><span class="sxs-lookup"><span data-stu-id="33dd9-109">Represents the progress of the print job.</span></span><br/>                                                                                                                                                                        |
| [<span data-ttu-id="33dd9-110">**IPrintDocumentPackageTarget**</span><span class="sxs-lookup"><span data-stu-id="33dd9-110">**IPrintDocumentPackageTarget**</span></span>](/windows/win32/api/documenttarget/nn-documenttarget-iprintdocumentpackagetarget)<br/>               | <span data-ttu-id="33dd9-111">可讓使用者列舉支援的封裝目標型別，並使用指定的類型識別碼建立一個。</span><span class="sxs-lookup"><span data-stu-id="33dd9-111">Allows users to enumerate the supported package target types and to create one with a given type ID.</span></span> <span data-ttu-id="33dd9-112">**IPrintDocumentPackageTarget** 也支援追蹤封裝列印進度和取消。</span><span class="sxs-lookup"><span data-stu-id="33dd9-112">**IPrintDocumentPackageTarget** also supports the tracking of the package printing progress and cancelling.</span></span><br/> |
| [<span data-ttu-id="33dd9-113">**IPrintDocumentPackageTargetFactory**</span><span class="sxs-lookup"><span data-stu-id="33dd9-113">**IPrintDocumentPackageTargetFactory**</span></span>](/windows/desktop/api/documenttarget/nn-documenttarget-iprintdocumentpackagetargetfactory)<br/> | <span data-ttu-id="33dd9-114">與 [IPrintDocumentPackageTarget](/windows/win32/api/documenttarget/nn-documenttarget-iprintdocumentpackagetarget) 搭配使用，以啟動列印工作。</span><span class="sxs-lookup"><span data-stu-id="33dd9-114">Used with [IPrintDocumentPackageTarget](/windows/win32/api/documenttarget/nn-documenttarget-iprintdocumentpackagetarget) for starting a print job.</span></span><br/>                                                                                                               |



 

 

