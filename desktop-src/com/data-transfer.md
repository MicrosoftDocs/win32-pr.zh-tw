---
title: 資料轉送
description: 資料轉送
ms.assetid: 26b16438-f940-4086-869e-74021ed00b1e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37dee268b99f205e0093288f6980c8425220a45b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507433"
---
# <a name="data-transfer"></a><span data-ttu-id="532b5-103">資料轉送</span><span class="sxs-lookup"><span data-stu-id="532b5-103">Data Transfer</span></span>

<span data-ttu-id="532b5-104">元件物件模型 (COM) 提供在應用程式之間傳輸資料的標準機制。</span><span class="sxs-lookup"><span data-stu-id="532b5-104">The Component Object Model (COM) provides a standard mechanism for transferring data between applications.</span></span> <span data-ttu-id="532b5-105">這項機制是 *資料物件*，只是任何會實 [**IDATAOBJECT**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) 介面的 COM 物件。</span><span class="sxs-lookup"><span data-stu-id="532b5-105">This mechanism is the *data object*, which is simply any COM object that implements the [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) interface.</span></span> <span data-ttu-id="532b5-106">某些資料物件（例如複製到剪貼簿的文字片段）具有 **IDataObject** 做為其唯一介面。</span><span class="sxs-lookup"><span data-stu-id="532b5-106">Some data objects, such as a piece of text copied to the clipboard, have **IDataObject** as their sole interface.</span></span> <span data-ttu-id="532b5-107">有些則會公開多個介面，例如複合檔案物件， **IDataObject** 只是一個。</span><span class="sxs-lookup"><span data-stu-id="532b5-107">Others, such as compound document objects, expose several interfaces, of which **IDataObject** is simply one.</span></span> <span data-ttu-id="532b5-108">資料物件是使用複合檔案的基礎，雖然它們在該 OLE 技術之外也有廣泛的應用程式。</span><span class="sxs-lookup"><span data-stu-id="532b5-108">Data objects are fundamental to the working of compound documents, although they also have widespread application outside that OLE technology.</span></span>

<span data-ttu-id="532b5-109">藉由交換資料物件的指標，資料的提供者和取用者就能以一致的方式管理資料傳輸，不論資料格式為何、用來傳送資料的媒體類型，或是要轉譯的目標裝置。</span><span class="sxs-lookup"><span data-stu-id="532b5-109">By exchanging pointers to a data object, providers and consumers of data can manage data transfers in a uniform manner, regardless of the format of the data, the type of medium used to transfer the data, or the target device on which it is to be rendered.</span></span> <span data-ttu-id="532b5-110">您可以在應用程式中包含基本剪貼簿傳輸的支援、拖放傳輸，以及使用單一 [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject)執行的 OLE 複合檔案傳輸。</span><span class="sxs-lookup"><span data-stu-id="532b5-110">You can include support in your application for basic clipboard transfers, drag and drop transfers, and OLE compound document transfers with a single implementation of [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject).</span></span> <span data-ttu-id="532b5-111">這麼做之後，需要用來容納每個通訊協定之特殊語義的程式碼數量很少。</span><span class="sxs-lookup"><span data-stu-id="532b5-111">Having done that, the amount of code required to accommodate the special semantics of each protocol is minimal.</span></span>

<span data-ttu-id="532b5-112">如需詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="532b5-112">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="532b5-113">資料傳輸介面</span><span class="sxs-lookup"><span data-stu-id="532b5-113">Data Transfer Interfaces</span></span>](data-transfer-interfaces.md)
-   [<span data-ttu-id="532b5-114">資料格式和傳輸媒體</span><span class="sxs-lookup"><span data-stu-id="532b5-114">Data Formats and Transfer Media</span></span>](data-formats-and-transfer-media.md)
-   [<span data-ttu-id="532b5-115">拖放功能</span><span class="sxs-lookup"><span data-stu-id="532b5-115">Drag and Drop</span></span>](drag-and-drop.md)

## <a name="related-topics"></a><span data-ttu-id="532b5-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="532b5-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="532b5-117">複合檔案</span><span class="sxs-lookup"><span data-stu-id="532b5-117">Compound Documents</span></span>](compound-documents.md)
</dt> </dl>

 

 




