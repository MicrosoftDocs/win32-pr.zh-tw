---
description: 當使用 SignTool 搭配-t 選項簽署檔案時，通常會包含時間戳記。
ms.assetid: ca22d055-dc34-447c-991b-27ff21ca3afc
title: 將時間戳記新增至先前簽署的檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef2e750dcb178b2a089bfbde0b2aea882b097c86
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/10/2021
ms.locfileid: "106999965"
---
# <a name="adding-time-stamps-to-previously-signed-files"></a><span data-ttu-id="d65c9-103">將時間戳記新增至先前簽署的檔案</span><span class="sxs-lookup"><span data-stu-id="d65c9-103">Adding Time Stamps to Previously Signed Files</span></span>

<span data-ttu-id="d65c9-104">當使用 SignTool 搭配 **-t** 選項簽署檔案時，通常會包含時間戳記。</span><span class="sxs-lookup"><span data-stu-id="d65c9-104">Time stamps are normally included when a file is signed using SignTool with the **-t** option.</span></span> <span data-ttu-id="d65c9-105">此外，您可以將時間戳記新增至未經過時間戳記簽署的檔案。</span><span class="sxs-lookup"><span data-stu-id="d65c9-105">In addition, time stamps can be added to files that were signed without a time stamp.</span></span> <span data-ttu-id="d65c9-106">下列命令會將時間戳記新增至先前簽署的檔案：</span><span class="sxs-lookup"><span data-stu-id="d65c9-106">The following command adds a time stamp to a previously signed file:</span></span>

<span data-ttu-id="d65c9-107">**signtool timestamp-t HTTPs： \/ /timestamp.digicert.com *MyControl.exe***</span><span class="sxs-lookup"><span data-stu-id="d65c9-107">**signtool timestamp -t https:\//timestamp.digicert.com *MyControl.exe***</span></span>

> [!Note]  
> <span data-ttu-id="d65c9-108">要加上時間戳記的檔案必須先前已簽署。</span><span class="sxs-lookup"><span data-stu-id="d65c9-108">The file to be time stamped must have previously been signed.</span></span>

 

<span data-ttu-id="d65c9-109">如需 SignTool 的詳細資訊，請參閱 [SignTool](signtool.md)。</span><span class="sxs-lookup"><span data-stu-id="d65c9-109">For more information about SignTool, see [SignTool](signtool.md).</span></span>

 

 



