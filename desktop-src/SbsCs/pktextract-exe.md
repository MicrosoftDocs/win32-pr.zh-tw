---
description: Pktextract.exe 是從憑證檔案中解壓縮 publicKeyToken 屬性的工具。
ms.assetid: 195ff5bd-bb60-4053-9308-ceacd29853c0
title: Pktextract.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd163efabd01d65969788aefc2386b2f49079729
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115185"
---
# <a name="pktextractexe"></a><span data-ttu-id="814bc-103">Pktextract.exe</span><span class="sxs-lookup"><span data-stu-id="814bc-103">Pktextract.exe</span></span>

<span data-ttu-id="814bc-104">Pktextract.exe 是從憑證檔案中解壓縮 **publicKeyToken** 屬性的工具。</span><span class="sxs-lookup"><span data-stu-id="814bc-104">Pktextract.exe is a tool that extracts the **publicKeyToken** attribute from a certificate file.</span></span> <span data-ttu-id="814bc-105">輸出是 **publicKeyToken**，也就是憑證中公開金鑰的唯一16個字元 (8 位元組) 識別碼，其格式可輕鬆地貼入元件身分識別語句中。</span><span class="sxs-lookup"><span data-stu-id="814bc-105">The output is the **publicKeyToken**, which is a unique 16-character (8-byte) identifier of the public key present in the certificate, in a format that can easily be pasted into an assembly identity statement.</span></span> <span data-ttu-id="814bc-106">憑證檔案必須存在於 Pktextract.exe 的相同目錄中，才能使用公用程式。</span><span class="sxs-lookup"><span data-stu-id="814bc-106">The certificate file must be present in the same directory as Pktextract.exe to use the utility.</span></span> <span data-ttu-id="814bc-107">Microsoft Windows 軟體開發套件 (SDK) 中提供 Pktextract.exe。</span><span class="sxs-lookup"><span data-stu-id="814bc-107">Pktextract.exe is provided in the Microsoft Windows Software Development Kit (SDK).</span></span>

## <a name="syntax"></a><span data-ttu-id="814bc-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="814bc-108">Syntax</span></span>

<span data-ttu-id="814bc-109">**pktextract.exe** *<檔案名 .cer>* **\[ -quiet \] \[ -nologo \]**</span><span class="sxs-lookup"><span data-stu-id="814bc-109">**pktextract.exe** *<filename.cer>* **\[-quiet\] \[-nologo\]**</span></span>

## <a name="command-line-options"></a><span data-ttu-id="814bc-110">命令列選項</span><span class="sxs-lookup"><span data-stu-id="814bc-110">Command Line Options</span></span>

<span data-ttu-id="814bc-111">Pktextract.exe 會使用下列不區分大小寫的命令列選項。</span><span class="sxs-lookup"><span data-stu-id="814bc-111">Pktextract.exe uses the following case-insensitive command line options.</span></span>



| <span data-ttu-id="814bc-112">選項</span><span class="sxs-lookup"><span data-stu-id="814bc-112">Option</span></span>  | <span data-ttu-id="814bc-113">Description</span><span class="sxs-lookup"><span data-stu-id="814bc-113">Description</span></span>                                                          |
|---------|----------------------------------------------------------------------|
| <span data-ttu-id="814bc-114">-quiet</span><span class="sxs-lookup"><span data-stu-id="814bc-114">-quiet</span></span>  | <span data-ttu-id="814bc-115">隱藏憑證資訊的完整顯示。</span><span class="sxs-lookup"><span data-stu-id="814bc-115">Suppresses full display of certificate information.</span></span> <span data-ttu-id="814bc-116">選擇性。</span><span class="sxs-lookup"><span data-stu-id="814bc-116">Optional.</span></span>        |
| <span data-ttu-id="814bc-117">-nologo</span><span class="sxs-lookup"><span data-stu-id="814bc-117">-nologo</span></span> | <span data-ttu-id="814bc-118">在不顯示標準 Microsoft 著作權資料的情況下執行。</span><span class="sxs-lookup"><span data-stu-id="814bc-118">Runs without displaying standard Microsoft copyright data.</span></span> <span data-ttu-id="814bc-119">選擇性。</span><span class="sxs-lookup"><span data-stu-id="814bc-119">Optional.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="814bc-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="814bc-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="814bc-121">並存元件開發工具</span><span class="sxs-lookup"><span data-stu-id="814bc-121">Side-by-Side Assembly Development Tools</span></span>](side-by-side-assembly-development-tools.md)
</dt> </dl>

 

 



