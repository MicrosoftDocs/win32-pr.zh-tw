---
description: 指定元件的物件表示函式字串
ms.assetid: 0c5aaaae-368e-4b3e-a483-b3a23c353e6e
title: 指定元件的物件表示函式字串
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ca4604d07a5b750d02a968456d33c9e5bc6bee8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847219"
---
# <a name="specifying-an-object-constructor-string-for-a-component"></a><span data-ttu-id="12f2d-103">指定元件的物件表示函式字串</span><span class="sxs-lookup"><span data-stu-id="12f2d-103">Specifying an Object Constructor String for a Component</span></span>

<span data-ttu-id="12f2d-104">若要指定元件的物件表示函式字串，請使用下列步驟：</span><span class="sxs-lookup"><span data-stu-id="12f2d-104">To specify an object constructor string for a component, use the following steps:</span></span>

1.  <span data-ttu-id="12f2d-105">在 [元件服務] 系統管理工具的詳細資料窗格中，以滑鼠 **按右鍵您** 要設定的元件，然後按一下 [內容]。</span><span class="sxs-lookup"><span data-stu-id="12f2d-105">In the details pane of the Component Services administrative tool, right-click the component that you want to configure and then click **Properties**.</span></span>
2.  <span data-ttu-id="12f2d-106">在 [元件屬性] 對話方塊中，按一下 [ **啟用** ] 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="12f2d-106">In the component properties dialog box, click the **Activation** tab.</span></span>
3.  <span data-ttu-id="12f2d-107">若要允許使用物件的 [函式] 字串，請選取 [ **啟用物件結構** ] 核取方塊。</span><span class="sxs-lookup"><span data-stu-id="12f2d-107">To enable use of the object constructor string, select the **Enable object construction** check box.</span></span>
4.  <span data-ttu-id="12f2d-108">在 [函式 **字串** ] 方塊中，輸入結構字串 (例如 DSN = AccountingServer) 。</span><span class="sxs-lookup"><span data-stu-id="12f2d-108">In the **Constructor string** box, enter the construction string (for example, DSN=AccountingServer).</span></span> <span data-ttu-id="12f2d-109">您可以選擇輸入空字串。</span><span class="sxs-lookup"><span data-stu-id="12f2d-109">You have the option of entering an empty string.</span></span>

> [!Note]  
> <span data-ttu-id="12f2d-110">物件的函式字串不應該用來儲存安全性機密資訊。</span><span class="sxs-lookup"><span data-stu-id="12f2d-110">Object constructor strings should not be used to store security-sensitive information.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="12f2d-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="12f2d-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="12f2d-112">COM + 物件的函數位符串概念</span><span class="sxs-lookup"><span data-stu-id="12f2d-112">COM+ Object Constructor Strings Concepts</span></span>](com--object-constructor-strings-concepts.md)
</dt> <dt>

[<span data-ttu-id="12f2d-113">使用物件的函式字串來建立元件</span><span class="sxs-lookup"><span data-stu-id="12f2d-113">Using an Object Constructor String to Construct a Component</span></span>](using-an-object-constructor-string-to-construct-a-component.md)
</dt> </dl>

 

 



