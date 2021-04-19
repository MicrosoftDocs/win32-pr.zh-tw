---
description: 受控物件格式 (MOF) 是用來描述通用訊息模型 (CIM) 類別的語言。
ms.assetid: 26494142-2078-4d46-a794-e43973255c2d
ms.tgt_platform: multiple
title: 管理物件格式 (MOF)
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 16f95c6868943a2f41c4326c341207ff26a03af6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106990389"
---
# <a name="managed-object-format-mof"></a><span data-ttu-id="23a37-103">管理物件格式 (MOF)</span><span class="sxs-lookup"><span data-stu-id="23a37-103">Managed Object Format (MOF)</span></span>

<span data-ttu-id="23a37-104">受控物件格式 (MOF) 是用來描述 [*通用訊息模型 (CIM)*](gloss-c.md) 類別的語言。</span><span class="sxs-lookup"><span data-stu-id="23a37-104">Managed Object Format (MOF) is the language used to describe [*Common Information Model (CIM)*](gloss-c.md) classes.</span></span>

<span data-ttu-id="23a37-105">針對 WMI 提供者執行新 WMI 類別的建議方式，是在使用 [**Mofcomp.exe**](mofcomp.md) 編譯至 [*wmi 存放庫*](gloss-w.md)的 MOF 檔案中。</span><span class="sxs-lookup"><span data-stu-id="23a37-105">The recommended way for WMI providers to implement new WMI classes is in MOF files which are compiled using [**Mofcomp.exe**](mofcomp.md) into the [*WMI repository*](gloss-w.md).</span></span> <span data-ttu-id="23a37-106">您也可以使用 [適用于 WMI 的 COM API](com-api-for-wmi.md)來建立和操作 CIM 類別和實例。</span><span class="sxs-lookup"><span data-stu-id="23a37-106">It is also possible to create and manipulate CIM classes and instances using the [COM API for WMI](com-api-for-wmi.md).</span></span>

<span data-ttu-id="23a37-107">WMI 提供者通常包含 MOF 檔案，該檔案會定義提供者傳回資料的資料和事件類別，以及包含提供資料之程式碼的 DLL 檔案。</span><span class="sxs-lookup"><span data-stu-id="23a37-107">A WMI provider normally consists of a MOF file, which defines the data and event classes for which the provider returns data, and a DLL file which contains the code that supplies data.</span></span> <span data-ttu-id="23a37-108">如需詳細資訊，請參閱 [將資料提供給 WMI](providing-data-to-wmi.md)。</span><span class="sxs-lookup"><span data-stu-id="23a37-108">For more information, see [Providing Data to WMI](providing-data-to-wmi.md).</span></span>

<span data-ttu-id="23a37-109">WMI 用戶端腳本和應用程式可以查詢提供者 MOF 類別的實例，或訂閱以接收事件通知。</span><span class="sxs-lookup"><span data-stu-id="23a37-109">WMI client scripts and applications can query for instances of provider MOF classes or subscribe to receive event notifications.</span></span>

<span data-ttu-id="23a37-110">您可以使用 MOF 來執行下列工作：</span><span class="sxs-lookup"><span data-stu-id="23a37-110">You can perform the following tasks with MOF:</span></span>

-   [<span data-ttu-id="23a37-111">編譯 MOF 檔案</span><span class="sxs-lookup"><span data-stu-id="23a37-111">Compiling MOF Files</span></span>](compiling-mof-files.md)
-   [<span data-ttu-id="23a37-112">建立類別</span><span class="sxs-lookup"><span data-stu-id="23a37-112">Creating a Class</span></span>](creating-a-class.md)
-   [<span data-ttu-id="23a37-113">建立實例</span><span class="sxs-lookup"><span data-stu-id="23a37-113">Creating an Instance</span></span>](creating-an-instance.md)
-   [<span data-ttu-id="23a37-114">建立方法</span><span class="sxs-lookup"><span data-stu-id="23a37-114">Creating a Method</span></span>](creating-a-method.md)
-   [<span data-ttu-id="23a37-115">新增限定詞</span><span class="sxs-lookup"><span data-stu-id="23a37-115">Adding a Qualifier</span></span>](adding-a-qualifier.md)
-   [<span data-ttu-id="23a37-116">建立批註</span><span class="sxs-lookup"><span data-stu-id="23a37-116">Creating a Comment</span></span>](creating-a-comment.md)

## <a name="related-topics"></a><span data-ttu-id="23a37-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="23a37-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="23a37-118">關於 WMI</span><span class="sxs-lookup"><span data-stu-id="23a37-118">About WMI</span></span>](about-wmi.md)
</dt> </dl>

 

 



