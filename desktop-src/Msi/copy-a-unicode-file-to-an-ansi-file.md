---
description: Windows Installer 開發人員 Windows SDK 元件中提供了 VBScript 檔案 WiToAnsi.vbs。 此範例說明如何使用腳本，將 Unicode 文字檔重寫為 ANSI 文字檔。
ms.assetid: cb22495f-968c-470a-a2f1-d0e068133956
title: 將 Unicode 檔案複製到 ANSI 檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bde68c60eaa5a007aee7d2ca2d79159c9b7fce20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849976"
---
# <a name="copy-a-unicode-file-to-an-ansi-file"></a><span data-ttu-id="83c5b-104">將 Unicode 檔案複製到 ANSI 檔案</span><span class="sxs-lookup"><span data-stu-id="83c5b-104">Copy a Unicode File to an ANSI File</span></span>

<span data-ttu-id="83c5b-105">[Windows Installer 開發人員 Windows SDK 元件](platform-sdk-components-for-windows-installer-developers.md)中提供了 VBScript 檔案 WiToAnsi.vbs。</span><span class="sxs-lookup"><span data-stu-id="83c5b-105">The VBScript file WiToAnsi.vbs is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="83c5b-106">此範例說明如何使用腳本，將 Unicode 文字檔重寫為 ANSI 文字檔。</span><span class="sxs-lookup"><span data-stu-id="83c5b-106">This sample shows how script is used to rewrite a Unicode text file as an ANSI text file.</span></span>

<span data-ttu-id="83c5b-107">使用此範例需要 Windows Script Host 的 CScript.exe 或 WScript.exe 版本。</span><span class="sxs-lookup"><span data-stu-id="83c5b-107">Using this sample requires the CScript.exe or WScript.exe version of Windows Script Host.</span></span> <span data-ttu-id="83c5b-108">若要使用 CScript.exe 執行此範例，請使用下列語法在命令提示字元中輸入命令列。</span><span class="sxs-lookup"><span data-stu-id="83c5b-108">To use CScript.exe to run this sample, type a command line at the command prompt using the following syntax.</span></span> <span data-ttu-id="83c5b-109">如果第一個引數是/？，則會顯示說明</span><span class="sxs-lookup"><span data-stu-id="83c5b-109">Help is displayed if the first argument is /?</span></span> <span data-ttu-id="83c5b-110">或者，如果指定的引數太少。</span><span class="sxs-lookup"><span data-stu-id="83c5b-110">or if too few arguments are specified.</span></span> <span data-ttu-id="83c5b-111">若要將輸出重新導向至檔案，請以 VBS > 路徑結束命令列 \[  \] 。</span><span class="sxs-lookup"><span data-stu-id="83c5b-111">To redirect the output to a file, end the command line with VBS > \[*path to file*\].</span></span> <span data-ttu-id="83c5b-112">此範例會傳回值0表示成功，如果叫用說明，則傳回 1; 如果腳本失敗，則傳回2。</span><span class="sxs-lookup"><span data-stu-id="83c5b-112">The sample returns a value of 0 for success, 1 if help is invoked, and 2 if the script fails.</span></span>

<span data-ttu-id="83c5b-113">**cscript WiToAnsi.vbs ANSI 檔案的 Unicode 檔案路徑 \[ 路徑 \] \[\]**</span><span class="sxs-lookup"><span data-stu-id="83c5b-113">**cscript WiToAnsi.vbs \[path to Unicode file\]\[path to ANSI file\]**</span></span>

<span data-ttu-id="83c5b-114">指定要轉換的 Unicode 文字檔。</span><span class="sxs-lookup"><span data-stu-id="83c5b-114">Specify the Unicode text file that is being converted.</span></span> <span data-ttu-id="83c5b-115">指定要建立的 ANSI 文字檔。</span><span class="sxs-lookup"><span data-stu-id="83c5b-115">Specify the ANSI text file that is being created.</span></span> <span data-ttu-id="83c5b-116">如果未指定 ANSI 檔案，則會取代 Unicode 檔案。</span><span class="sxs-lookup"><span data-stu-id="83c5b-116">If no ANSI file is specified, the Unicode file is replaced.</span></span>

<span data-ttu-id="83c5b-117">如需其他腳本範例，請參閱 [Windows Installer 腳本範例](windows-installer-scripting-examples.md)。</span><span class="sxs-lookup"><span data-stu-id="83c5b-117">For additional scripting examples, see [Windows Installer Scripting Examples](windows-installer-scripting-examples.md).</span></span> <span data-ttu-id="83c5b-118">針對不需要 Windows Script Host 的範例公用程式，請參閱 [Windows Installer 開發工具](windows-installer-development-tools.md)。</span><span class="sxs-lookup"><span data-stu-id="83c5b-118">For sample utilities that do not require Windows Script Host see [Windows Installer Development Tools](windows-installer-development-tools.md).</span></span>

 

 



