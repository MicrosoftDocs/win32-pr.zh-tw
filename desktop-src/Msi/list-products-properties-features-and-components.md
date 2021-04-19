---
description: Windows Installer 開發人員 Windows SDK 元件中提供了 VBScript 檔案 WiLstPrd.vbs。 範例腳本會連接到安裝程式物件，並列舉已註冊的產品和產品資訊。
ms.assetid: 13615dc2-ebc7-4536-9dd8-9bb1dbf3cfaf
title: 列出產品、屬性、功能和元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e20d2f563efad42108f763b909e7a1118e255dcb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972230"
---
# <a name="list-products-properties-features-and-components"></a><span data-ttu-id="38278-104">列出產品、屬性、功能和元件</span><span class="sxs-lookup"><span data-stu-id="38278-104">List Products, Properties, Features, and Components</span></span>

<span data-ttu-id="38278-105">[Windows Installer 開發人員 Windows SDK 元件](platform-sdk-components-for-windows-installer-developers.md)中提供了 VBScript 檔案 WiLstPrd.vbs。</span><span class="sxs-lookup"><span data-stu-id="38278-105">The VBScript file WiLstPrd.vbs is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="38278-106">範例腳本會連接到 [**安裝程式**](installer-object.md) 物件，並列舉已註冊的產品和產品資訊。</span><span class="sxs-lookup"><span data-stu-id="38278-106">The sample script connects to an [**Installer**](installer-object.md) object and enumerates registered products and product information.</span></span>

<span data-ttu-id="38278-107">這個範例示範如何使用：</span><span class="sxs-lookup"><span data-stu-id="38278-107">This sample demonstrates the use of:</span></span>

-   [<span data-ttu-id="38278-108">**ProductInfo 屬性**</span><span class="sxs-lookup"><span data-stu-id="38278-108">**ProductInfo property**</span></span>](installer-productinfo.md)
-   [<span data-ttu-id="38278-109">**ProductState 屬性 (安裝程式物件)**</span><span class="sxs-lookup"><span data-stu-id="38278-109">**ProductState property (Installer object)**</span></span>](installer-productstate-property.md)
-   [<span data-ttu-id="38278-110">**Products 屬性**</span><span class="sxs-lookup"><span data-stu-id="38278-110">**Products property**</span></span>](installer-products.md)
-   [<span data-ttu-id="38278-111">**Features 屬性**</span><span class="sxs-lookup"><span data-stu-id="38278-111">**Features property**</span></span>](installer-features.md)
-   [<span data-ttu-id="38278-112">**FeatureParent 屬性**</span><span class="sxs-lookup"><span data-stu-id="38278-112">**FeatureParent property**</span></span>](installer-featureparent.md)
-   [<span data-ttu-id="38278-113">**FeatureState 屬性**</span><span class="sxs-lookup"><span data-stu-id="38278-113">**FeatureState property**</span></span>](installer-featurestate.md)
-   [<span data-ttu-id="38278-114">**元件屬性**</span><span class="sxs-lookup"><span data-stu-id="38278-114">**Components property**</span></span>](installer-components.md)
-   [<span data-ttu-id="38278-115">**ComponentClients 屬性**</span><span class="sxs-lookup"><span data-stu-id="38278-115">**ComponentClients property**</span></span>](installer-componentclients.md)
-   [<span data-ttu-id="38278-116">**ComponentPath 屬性**</span><span class="sxs-lookup"><span data-stu-id="38278-116">**ComponentPath property**</span></span>](installer-componentpath.md)
-   [<span data-ttu-id="38278-117">**LastErrorRecord 方法**</span><span class="sxs-lookup"><span data-stu-id="38278-117">**LastErrorRecord method**</span></span>](installer-lasterrorrecord.md)
-   <span data-ttu-id="38278-118">[](installer-registryvalue.md) [**安裝程式物件** 的 RegistryValue 方法](installer-object.md)</span><span class="sxs-lookup"><span data-stu-id="38278-118">[**RegistryValue method**](installer-registryvalue.md) of the [**Installer object**](installer-object.md)</span></span>

<span data-ttu-id="38278-119">您將需要 CScript.exe 或 WScript.exe 版本的 Windows Script Host 才能使用此範例。</span><span class="sxs-lookup"><span data-stu-id="38278-119">You'll require the CScript.exe or WScript.exe version of Windows Script Host to use this sample.</span></span> <span data-ttu-id="38278-120">若要使用 CScript.exe 執行此範例，請使用下列語法在命令提示字元中輸入命令列。</span><span class="sxs-lookup"><span data-stu-id="38278-120">To use CScript.exe to run this sample, type a command line at the command prompt using the following syntax.</span></span> <span data-ttu-id="38278-121">如果第一個引數是/？，則會顯示說明</span><span class="sxs-lookup"><span data-stu-id="38278-121">Help is displayed if the first argument is /?</span></span> <span data-ttu-id="38278-122">或者，如果指定的引數太少。</span><span class="sxs-lookup"><span data-stu-id="38278-122">or if too few arguments are specified.</span></span> <span data-ttu-id="38278-123">若要將輸出重新導向至檔案，請以 VBS > 路徑結束命令列 \[ \] 。</span><span class="sxs-lookup"><span data-stu-id="38278-123">To redirect the output to a file, end the command line with VBS > \[path to file\].</span></span> <span data-ttu-id="38278-124">此範例會傳回值0表示成功，如果叫用說明，則傳回 1; 如果腳本失敗，則傳回2。</span><span class="sxs-lookup"><span data-stu-id="38278-124">The sample returns a value of 0 for success, 1 if help is invoked, and 2 if the script fails.</span></span>

<span data-ttu-id="38278-125">**cscript WiLstPrd.vbs \[ 產品名稱 \] \[ 選項\]**</span><span class="sxs-lookup"><span data-stu-id="38278-125">**cscript WiLstPrd.vbs \[Product Name\] \[options\]**</span></span>

<span data-ttu-id="38278-126">指定不區分大小寫的產品名稱或已安裝或已公告產品的產品識別碼 GUID。</span><span class="sxs-lookup"><span data-stu-id="38278-126">Specify the case-insensitive product name or the product ID GUID of the installed or advertised product.</span></span> <span data-ttu-id="38278-127">如果未指定任何產品或選項，安裝程式會列出系統上安裝或公告的所有產品。</span><span class="sxs-lookup"><span data-stu-id="38278-127">If no product or options are specified, the installer lists all the products installed or advertised on the system.</span></span>

<span data-ttu-id="38278-128">請注意，這些選項不是參數，因此您不應該在命令列上以斜線 (/) 作為前置詞。</span><span class="sxs-lookup"><span data-stu-id="38278-128">Note that these options are not switches so you should not prefix them with a slash (/) on the commandline.</span></span> <span data-ttu-id="38278-129">您可以串連字母來結合下列選項。</span><span class="sxs-lookup"><span data-stu-id="38278-129">The following options may be combined by concatenating the letters.</span></span> <span data-ttu-id="38278-130">例如，"pc" 可列出產品的屬性和已安裝的元件。</span><span class="sxs-lookup"><span data-stu-id="38278-130">For example, "pc" to list both the products' properties and installed components.</span></span>



| <span data-ttu-id="38278-131">選項</span><span class="sxs-lookup"><span data-stu-id="38278-131">Option</span></span>               | <span data-ttu-id="38278-132">Description</span><span class="sxs-lookup"><span data-stu-id="38278-132">Description</span></span>                                                                                                                           |
|----------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38278-133">未指定任何選項</span><span class="sxs-lookup"><span data-stu-id="38278-133">no options specified</span></span> | <span data-ttu-id="38278-134">列出產品的屬性。</span><span class="sxs-lookup"><span data-stu-id="38278-134">List the products' properties.</span></span>                                                                                                        |
| <span data-ttu-id="38278-135">p</span><span class="sxs-lookup"><span data-stu-id="38278-135">p</span></span>                    | <span data-ttu-id="38278-136">列出產品的屬性。</span><span class="sxs-lookup"><span data-stu-id="38278-136">List the products' properties.</span></span>                                                                                                        |
| <span data-ttu-id="38278-137">f</span><span class="sxs-lookup"><span data-stu-id="38278-137">f</span></span>                    | <span data-ttu-id="38278-138">列出產品的功能、功能父系和安裝狀態</span><span class="sxs-lookup"><span data-stu-id="38278-138">List the products' features, feature parents, and installation states</span></span>                                                                 |
| <span data-ttu-id="38278-139">c</span><span class="sxs-lookup"><span data-stu-id="38278-139">c</span></span>                    | <span data-ttu-id="38278-140">列出產品的已安裝元件。</span><span class="sxs-lookup"><span data-stu-id="38278-140">List the products' installed components.</span></span>                                                                                              |
| <span data-ttu-id="38278-141">d</span><span class="sxs-lookup"><span data-stu-id="38278-141">d</span></span>                    | <span data-ttu-id="38278-142">列出 [products **Software Microsoft Windows CurrentVersion shareddll for products Software of Software] 元件的 [HKLM \\ Software \\ Microsoft \\ Windows \\ \\** ] 下的值。</span><span class="sxs-lookup"><span data-stu-id="38278-142">List the value under **HKLM\\Software\\Microsoft\\Windows\\CurrentVersion\\SharedDlls** for the key files of the products' component.</span></span> |



 

<span data-ttu-id="38278-143">如需詳細資訊，請參閱 [Windows Installer 腳本範例](windows-installer-scripting-examples.md) ，以取得其他腳本範例。</span><span class="sxs-lookup"><span data-stu-id="38278-143">For more information, see [Windows Installer Scripting Examples](windows-installer-scripting-examples.md) for additional scripting examples.</span></span> <span data-ttu-id="38278-144">如需不需要 Windows Script Host 的範例公用程式，請參閱 [Windows Installer 開發工具](windows-installer-development-tools.md)。</span><span class="sxs-lookup"><span data-stu-id="38278-144">For sample utilities that do not require Windows Script Host, see [Windows Installer Development Tools](windows-installer-development-tools.md).</span></span>

 

 



