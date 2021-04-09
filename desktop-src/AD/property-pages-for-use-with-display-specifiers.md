---
title: 搭配顯示規範使用的屬性頁
description: Active Directory Domain Services 提供一種機制，讓您可以從 Active Directory 系統管理嵌入式管理單元或 Windows shell，將頁面新增至針對目錄物件所顯示的屬性工作表。
ms.assetid: c1dd84e2-50f9-4903-a4b5-4473515e4d0e
ms.tgt_platform: multiple
keywords:
- 顯示指定名稱 AD、屬性頁以用於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c204f4d378e66cda5bc02684cb51cc707ba3d6f2
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "103842047"
---
# <a name="property-pages-for-use-with-display-specifiers"></a><span data-ttu-id="4501f-104">搭配顯示規範使用的屬性頁</span><span class="sxs-lookup"><span data-stu-id="4501f-104">Property Pages for Use with Display Specifiers</span></span>

<span data-ttu-id="4501f-105">Active Directory Domain Services 提供一種機制，讓您可以從 Active Directory 系統管理嵌入式管理單元或 Windows shell，將頁面新增至針對目錄物件所顯示的屬性工作表。</span><span class="sxs-lookup"><span data-stu-id="4501f-105">Active Directory Domain Services provide a mechanism for adding pages to the property sheet displayed for a directory object from the Active Directory administrative snap-ins or the Windows shell.</span></span> <span data-ttu-id="4501f-106">若要將頁面加入至屬性工作表，請執行屬性工作表延伸。</span><span class="sxs-lookup"><span data-stu-id="4501f-106">To add a page to the property sheet, implement a property sheet extension.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="4501f-107">開發人員讀者</span><span class="sxs-lookup"><span data-stu-id="4501f-107">Developer Audience</span></span>

<span data-ttu-id="4501f-108">本檔假設讀者已熟悉使用 c + + 的 COM 作業和元件開發。</span><span class="sxs-lookup"><span data-stu-id="4501f-108">This documentation assumes that the reader is familiar with COM operation and component development using C++.</span></span> <span data-ttu-id="4501f-109">目前無法使用 Visual Basic 建立 Active Directory 的屬性工作表延伸模組。</span><span class="sxs-lookup"><span data-stu-id="4501f-109">It is not currently possible to create an Active Directory property sheet extension using Visual Basic.</span></span>

## <a name="creating-an-active-directory-property-sheet-extension"></a><span data-ttu-id="4501f-110">建立 Active Directory 屬性工作表延伸模組</span><span class="sxs-lookup"><span data-stu-id="4501f-110">Creating an Active Directory Property Sheet Extension</span></span>

<span data-ttu-id="4501f-111">*屬性工作表延伸* 模組是內部進程伺服器，會執行特定的介面並向 Active Directory Domain Services 註冊。</span><span class="sxs-lookup"><span data-stu-id="4501f-111">A *property sheet extension* is a COM in-proc server that implements certain interfaces and is registered with Active Directory Domain Services.</span></span> <span data-ttu-id="4501f-112">若要建立屬性工作表延伸模組，請執行下列步驟。</span><span class="sxs-lookup"><span data-stu-id="4501f-112">To create a property sheet extension, perform the following steps.</span></span>

<span data-ttu-id="4501f-113">**若要建立 Active Directory 屬性工作表延伸模組**</span><span class="sxs-lookup"><span data-stu-id="4501f-113">**To create an Active Directory property sheet extension**</span></span>

1.  <span data-ttu-id="4501f-114">建立屬性工作表延伸模組 DLL。</span><span class="sxs-lookup"><span data-stu-id="4501f-114">Create the property sheet extension DLL.</span></span> <span data-ttu-id="4501f-115">屬性工作表延伸是 COM 的內部伺服器伺服器，至少會執行 [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) 和 [**IShellPropSheetExt**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext) 介面。</span><span class="sxs-lookup"><span data-stu-id="4501f-115">A property sheet extension is a COM in-proc server that, at a minimum, implements the [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) and [**IShellPropSheetExt**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext) interfaces.</span></span> <span data-ttu-id="4501f-116">如需詳細資訊，請參閱 [執行屬性頁面 COM 物件](implementing-the-property-page-com-object.md)。</span><span class="sxs-lookup"><span data-stu-id="4501f-116">For more information, see [Implementing the Property Page COM Object](implementing-the-property-page-com-object.md).</span></span>
2.  <span data-ttu-id="4501f-117">在要使用屬性工作表擴充功能的電腦上安裝屬性工作表延伸模組。</span><span class="sxs-lookup"><span data-stu-id="4501f-117">Install the property sheet extension on the computers where the property sheet extension is to be used.</span></span> <span data-ttu-id="4501f-118">若要這樣做，請為屬性工作表延伸 DLL 建立 Microsoft Windows Installer 套件，並使用群組原則適當地部署套件。</span><span class="sxs-lookup"><span data-stu-id="4501f-118">To do this, create a Microsoft Windows Installer package for the property sheet extension DLL and deploy the package appropriately using the group policy.</span></span> <span data-ttu-id="4501f-119">如需詳細資訊，請參閱散發 [消費者介面元件](distributing-user-interface-components.md)。</span><span class="sxs-lookup"><span data-stu-id="4501f-119">For more information, see [Distributing User Interface Components](distributing-user-interface-components.md).</span></span>
3.  <span data-ttu-id="4501f-120">在 Windows 登錄和 Active Directory Domain Services 中註冊屬性工作表延伸模組。</span><span class="sxs-lookup"><span data-stu-id="4501f-120">Register the property sheet extension in the Windows registry and with Active Directory Domain Services.</span></span> <span data-ttu-id="4501f-121">如需詳細資訊，請參閱 [在顯示規範中註冊屬性頁 COM 物件](registering-the-property-page-com-object-in-a-display-specifier.md)。</span><span class="sxs-lookup"><span data-stu-id="4501f-121">For more information, see [Registering the Property Page COM Object in a Display Specifier](registering-the-property-page-com-object-in-a-display-specifier.md).</span></span>

 

 