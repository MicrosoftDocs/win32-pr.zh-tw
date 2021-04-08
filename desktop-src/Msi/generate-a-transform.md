---
description: Windows Installer 開發人員 Windows SDK 元件中提供了 VBScript 檔案 WiGenXfm.vbs。 此範例腳本可從兩個 Windows Installer 資料庫產生轉換。 如需詳細資訊，請參閱資料庫轉換。
ms.assetid: bfa918b8-8d90-4e14-8a06-6c3d5b5dc13b
title: 產生轉換
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92617c2e007b9deb01685679d4940095285b8218
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103693736"
---
# <a name="generate-a-transform"></a><span data-ttu-id="69d6f-105">產生轉換</span><span class="sxs-lookup"><span data-stu-id="69d6f-105">Generate a Transform</span></span>

<span data-ttu-id="69d6f-106">[Windows Installer 開發人員 Windows SDK 元件](platform-sdk-components-for-windows-installer-developers.md)中提供了 VBScript 檔案 WiGenXfm.vbs。</span><span class="sxs-lookup"><span data-stu-id="69d6f-106">The VBScript file WiGenXfm.vbs is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="69d6f-107">此範例腳本可從兩個 Windows Installer 資料庫產生轉換。</span><span class="sxs-lookup"><span data-stu-id="69d6f-107">This sample script can generate a transform from two Windows Installer databases.</span></span> <span data-ttu-id="69d6f-108">如需詳細資訊，請參閱 [資料庫轉換](database-transforms.md)。</span><span class="sxs-lookup"><span data-stu-id="69d6f-108">For more information see [Database Transforms](database-transforms.md).</span></span>

<span data-ttu-id="69d6f-109">此範例將示範如何使用：</span><span class="sxs-lookup"><span data-stu-id="69d6f-109">The sample demonstrates the use of:</span></span>

[<span data-ttu-id="69d6f-110">**(安裝程式物件) 的 OpenDatabase 方法**</span><span class="sxs-lookup"><span data-stu-id="69d6f-110">**OpenDatabase method (Installer Object)**</span></span>](installer-opendatabase.md)

<span data-ttu-id="69d6f-111">[](installer-lasterrorrecord.md) [**安裝程式物件** 的 LastErrorRecord 方法](installer-object.md)</span><span class="sxs-lookup"><span data-stu-id="69d6f-111">[**LastErrorRecord method**](installer-lasterrorrecord.md) of the [**Installer object**](installer-object.md)</span></span>

<span data-ttu-id="69d6f-112">[](database-generatetransform.md) [**資料庫物件** 的「進行」（method）方法](database-object.md)</span><span class="sxs-lookup"><span data-stu-id="69d6f-112">[**GenerateTransform method**](database-generatetransform.md) of the [**Database object**](database-object.md)</span></span>

<span data-ttu-id="69d6f-113">您將需要 CScript.exe 或 WScript.exe 版本的 Windows Script Host 才能使用此範例。</span><span class="sxs-lookup"><span data-stu-id="69d6f-113">You'll require the CScript.exe or WScript.exe version of Windows Script Host to use this sample.</span></span> <span data-ttu-id="69d6f-114">若要使用 CScript.exe 執行此範例，請使用下列語法在命令提示字元中輸入命令列。</span><span class="sxs-lookup"><span data-stu-id="69d6f-114">To use CScript.exe to run this sample, type a command line at the command prompt using the following syntax.</span></span> <span data-ttu-id="69d6f-115">如果第一個引數是/？，則會顯示說明</span><span class="sxs-lookup"><span data-stu-id="69d6f-115">Help is displayed if the first argument is /?</span></span> <span data-ttu-id="69d6f-116">或者，如果指定的引數太少。</span><span class="sxs-lookup"><span data-stu-id="69d6f-116">or if too few arguments are specified.</span></span> <span data-ttu-id="69d6f-117">若要將輸出重新導向至檔案，請以 VBS > 路徑結束命令列 \[  \] 。</span><span class="sxs-lookup"><span data-stu-id="69d6f-117">To redirect the output to a file, end the command line with VBS > \[*path to file*\].</span></span> <span data-ttu-id="69d6f-118">此範例會傳回值0表示成功，如果叫用說明，則傳回 1; 如果腳本失敗，則傳回2。</span><span class="sxs-lookup"><span data-stu-id="69d6f-118">The sample returns a value of 0 for success, 1 if help is invoked, and 2 if the script fails.</span></span>

<span data-ttu-id="69d6f-119">**cscript WiGenXfm.vbs \[ 原始資料庫路徑的路徑，以 \] \[ 修改轉換檔案的資料庫 \] \[ 路徑\]**</span><span class="sxs-lookup"><span data-stu-id="69d6f-119">**cscript WiGenXfm.vbs \[path to original database\]\[path to revised database\]\[path to transform file\]**</span></span>

<span data-ttu-id="69d6f-120">指定原始 Windows Installer 資料庫的路徑。</span><span class="sxs-lookup"><span data-stu-id="69d6f-120">Specify the path to the original Windows Installer database.</span></span> <span data-ttu-id="69d6f-121">指定已修改之資料庫的路徑。</span><span class="sxs-lookup"><span data-stu-id="69d6f-121">Specify the path to the revised database.</span></span> <span data-ttu-id="69d6f-122">指定要建立之轉換檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="69d6f-122">Specify the path to the transform file to be created.</span></span> <span data-ttu-id="69d6f-123">如果省略轉換檔的路徑，則只會比較兩個資料庫。</span><span class="sxs-lookup"><span data-stu-id="69d6f-123">If the path to the transform file is omitted, the two databases are only compared.</span></span>

<span data-ttu-id="69d6f-124">如需其他腳本範例，請參閱 [Windows Installer 腳本範例](windows-installer-scripting-examples.md)。</span><span class="sxs-lookup"><span data-stu-id="69d6f-124">For additional scripting examples, see [Windows Installer Scripting Examples](windows-installer-scripting-examples.md).</span></span> <span data-ttu-id="69d6f-125">如需不需要 Windows Script Host 的範例公用程式，請參閱 [Windows Installer 開發工具](windows-installer-development-tools.md)。</span><span class="sxs-lookup"><span data-stu-id="69d6f-125">For sample utilities that do not require Windows Script Host, see [Windows Installer Development Tools](windows-installer-development-tools.md).</span></span>

<span data-ttu-id="69d6f-126">請注意， [當地語系化範例](a-localization-example.md) 會示範如何 [產生自訂轉換](generating-a-customization-transform.md)。</span><span class="sxs-lookup"><span data-stu-id="69d6f-126">Note that [A Localization Example](a-localization-example.md) demonstrates [Generating a Customization Transform](generating-a-customization-transform.md).</span></span>

 

 



