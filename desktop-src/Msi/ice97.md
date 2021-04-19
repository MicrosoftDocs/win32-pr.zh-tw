---
description: ICE97 會確認兩個元件沒有將共用元件隔離到相同的目錄。
ms.assetid: 76eeb238-02a1-43c1-a3d7-5178e3c3eaee
title: ICE97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34c41701ce04c0071d6599f888083dfbea4bfc0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106974497"
---
# <a name="ice97"></a><span data-ttu-id="a9b4f-103">ICE97</span><span class="sxs-lookup"><span data-stu-id="a9b4f-103">ICE97</span></span>

<span data-ttu-id="a9b4f-104">ICE97 會確認兩個元件沒有將共用元件隔離到相同的目錄。</span><span class="sxs-lookup"><span data-stu-id="a9b4f-104">ICE97 verifies that two components do not isolate a shared component to the same directory.</span></span>

## <a name="result"></a><span data-ttu-id="a9b4f-105">結果</span><span class="sxs-lookup"><span data-stu-id="a9b4f-105">Result</span></span>

<span data-ttu-id="a9b4f-106">ICE97 會張貼下列警告。</span><span class="sxs-lookup"><span data-stu-id="a9b4f-106">ICE97 posts the following warnings.</span></span>



| <span data-ttu-id="a9b4f-107">ICE97 警告</span><span class="sxs-lookup"><span data-stu-id="a9b4f-107">ICE97 Warning</span></span>                                                                                                                                                                    | <span data-ttu-id="a9b4f-108">Description</span><span class="sxs-lookup"><span data-stu-id="a9b4f-108">Description</span></span>                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <span data-ttu-id="a9b4f-109">此元件 \[ 1 \] 會將共用的元件安裝到與 \[ 另一個相同的目錄 2 \] 中，如果已選取 (或更多) 元件進行安裝，則會中斷元件規則。</span><span class="sxs-lookup"><span data-stu-id="a9b4f-109">This component \[1\] installs the Shared component into the same directory \[2\] as another, which breaks component rules if both (or more) components are selected for install.</span></span> | <span data-ttu-id="a9b4f-110">兩個元件不得將共用元件隔離到相同的目錄。</span><span class="sxs-lookup"><span data-stu-id="a9b4f-110">Two components must not isolate a shared component to the same directory.</span></span> |



 

<span data-ttu-id="a9b4f-111">例如，Component1 和 Component2 （共用的 ComponentShared）會安裝在相同的目錄中。</span><span class="sxs-lookup"><span data-stu-id="a9b4f-111">For example, Component1 and Component2, which share ComponentShared, are installed to the same directory.</span></span> <span data-ttu-id="a9b4f-112">兩者都會將 ComponentShared 指定為隔離的元件。</span><span class="sxs-lookup"><span data-stu-id="a9b4f-112">Both specify ComponentShared as an isolated component.</span></span> <span data-ttu-id="a9b4f-113">由於隔離的原因，ComponentShared 中的檔案會複製兩次到 \_ Component1 和 Component2 的目錄參考中。</span><span class="sxs-lookup"><span data-stu-id="a9b4f-113">Because of the isolation, the files in ComponentShared are copied twice into the Directory\_ reference for Component1 and Component2.</span></span> <span data-ttu-id="a9b4f-114">元件的複本上現在有一個參考計數。</span><span class="sxs-lookup"><span data-stu-id="a9b4f-114">The components now have one reference count on the copy of files.</span></span> <span data-ttu-id="a9b4f-115">這違反了安裝程式元件規則。</span><span class="sxs-lookup"><span data-stu-id="a9b4f-115">This is in violation of the Installer component rules.</span></span> <span data-ttu-id="a9b4f-116">如果卸載 Component1，則會移除隔離的元件檔案，而 Component2 會中斷。</span><span class="sxs-lookup"><span data-stu-id="a9b4f-116">If Component1 is uninstalled, the isolated components files are removed and Component2 is broken.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a9b4f-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="a9b4f-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a9b4f-118">ICE 參考</span><span class="sxs-lookup"><span data-stu-id="a9b4f-118">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



