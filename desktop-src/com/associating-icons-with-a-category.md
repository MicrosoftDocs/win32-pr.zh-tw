---
title: 將圖示與類別產生關聯
description: 將圖示與類別產生關聯
ms.assetid: 5e5c3c10-07cf-4a34-9822-97ec940b3117
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98c7a662ab3aaf578f037ff246207d03e4fcd688
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104020975"
---
# <a name="associating-icons-with-a-category"></a><span data-ttu-id="85a90-103">將圖示與類別產生關聯</span><span class="sxs-lookup"><span data-stu-id="85a90-103">Associating Icons with a Category</span></span>

<span data-ttu-id="85a90-104">建立使用者介面，讓使用者能夠選取類別內的元件類別目錄，需要能夠針對特定類別目錄顯示有意義的影像。</span><span class="sxs-lookup"><span data-stu-id="85a90-104">Building a user interface that allows the user to select component categories within a category requires the ability to display a meaningful image for a particular category.</span></span> <span data-ttu-id="85a90-105">若要將圖示與元件類別建立關聯，請建立類別的 CATID 的金鑰，並使用 [DefaultIcon](defaulticon.md) 子機碼填入該金鑰。</span><span class="sxs-lookup"><span data-stu-id="85a90-105">To associate an icon with a component category, create a key for the category's CATID and populate that key with a [DefaultIcon](defaulticon.md) subkey.</span></span> <span data-ttu-id="85a90-106">登錄專案如下所示：</span><span class="sxs-lookup"><span data-stu-id="85a90-106">The registry entry is as follows:</span></span>

``` syntax
HKEY_CLASSES_ROOT\CLSID\{...catid...}\DefaultIcon = "c:\hello\icons.dll,1"
 
```

<span data-ttu-id="85a90-107">DefaultIcon 索引鍵所參考的檔案名可以是 EXE 或 DLL 檔案 (僅限資源的 DLL) 。</span><span class="sxs-lookup"><span data-stu-id="85a90-107">The filename referenced by the DefaultIcon key can be either an EXE or a DLL file (resource-only DLL).</span></span>

<span data-ttu-id="85a90-108">若要建立小型 16x16 "工具箱點陣圖與元件類別之間的關聯，請在類別的 CATID 的 **HKEY \_ 類別 \_ 根 \\ CLSID** 中建立索引鍵，並使用 [ToolBoxBitmap32](toolboxbitmap32.md) 子機碼填入該索引鍵，如下列範例所示：</span><span class="sxs-lookup"><span data-stu-id="85a90-108">To associate a small 16x16 "toolbox bitmap" with a component category, create a key in **HKEY\_CLASSES\_ROOT\\CLSID** for the category's CATID and populate that key with a [ToolBoxBitmap32](toolboxbitmap32.md) subkey, as shown in the following example:</span></span>

``` syntax
HKEY_CLASSES_ROOT\CLSID\{...catid...}\ToolBoxBitmap32 = "c:\goodbye\mycomponent.dll,42"
 
```

<span data-ttu-id="85a90-109">[ToolBoxBitmap32](toolboxbitmap32.md)索引鍵所參考的檔案名也可以是 EXE 或 dll 檔案 (僅限資源的 DLL) 。</span><span class="sxs-lookup"><span data-stu-id="85a90-109">The filename referenced by the [ToolBoxBitmap32](toolboxbitmap32.md) key can also be an EXE or DLL file (resource-only DLL).</span></span>

## <a name="related-topics"></a><span data-ttu-id="85a90-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="85a90-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="85a90-111">依元件功能分類</span><span class="sxs-lookup"><span data-stu-id="85a90-111">Categorizing by Component Capabilities</span></span>](categorizing-by-component-capabilities.md)
</dt> <dt>

[<span data-ttu-id="85a90-112">依容器功能分類</span><span class="sxs-lookup"><span data-stu-id="85a90-112">Categorizing by Container Capabilities</span></span>](categorizing-by-container-capabilities.md)
</dt> <dt>

[<span data-ttu-id="85a90-113">預設類別和關聯</span><span class="sxs-lookup"><span data-stu-id="85a90-113">Default Classes and Associations</span></span>](default-classes-and-associations.md)
</dt> <dt>

[<span data-ttu-id="85a90-114">定義元件類別</span><span class="sxs-lookup"><span data-stu-id="85a90-114">Defining Component Categories</span></span>](defining-component-categories.md)
</dt> <dt>

[<span data-ttu-id="85a90-115">**ICatInformation**</span><span class="sxs-lookup"><span data-stu-id="85a90-115">**ICatInformation**</span></span>](/windows/desktop/api/ComCat/nn-comcat-icatinformation)
</dt> <dt>

[<span data-ttu-id="85a90-116">**ICatRegister**</span><span class="sxs-lookup"><span data-stu-id="85a90-116">**ICatRegister**</span></span>](/windows/desktop/api/ComCat/nn-comcat-icatregister)
</dt> <dt>

[<span data-ttu-id="85a90-117">元件類別管理員</span><span class="sxs-lookup"><span data-stu-id="85a90-117">The Component Categories Manager</span></span>](the-component-categories-manager.md)
</dt> </dl>

 

 




