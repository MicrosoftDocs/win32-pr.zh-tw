---
title: 重新命名已編譯的資源檔
description: 根據預設，在編譯資源時，RC 會將編譯過的資源命名 ( .res) 檔案中，並以 .rc 檔的基底名稱取代，並將它放在與 .rc 檔案相同的目錄中。
ms.assetid: be120032-666f-4627-8f98-96bde7c55fa4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c54e22cff753dbc59cbce61cd71874c8fe77a85
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183060"
---
# <a name="renaming-the-compiled-resource-file"></a><span data-ttu-id="c812c-103">重新命名已編譯的資源檔</span><span class="sxs-lookup"><span data-stu-id="c812c-103">Renaming the Compiled Resource File</span></span>

<span data-ttu-id="c812c-104">根據預設，在編譯資源時，RC 會將編譯過的資源命名 ( .res) 檔案中，並以 .rc 檔的基底名稱取代，並將它放在與 .rc 檔案相同的目錄中。</span><span class="sxs-lookup"><span data-stu-id="c812c-104">By default, when compiling resources, RC names the compiled resource (.res) file with the base name of the .rc file and places it in the same directory as the .rc file.</span></span> <span data-ttu-id="c812c-105">接著，必須叫用 CVTRES，將 .res 檔轉換成二進位資源 (. rbj) 格式，可供連結器理解。</span><span class="sxs-lookup"><span data-stu-id="c812c-105">CVTRES must then be invoked to convert the .res file to a binary resource (.rbj) format which can be understood by the linker.</span></span> <span data-ttu-id="c812c-106">下列範例會編譯 MyApp，並在 MyApp. rc 的相同目錄中建立名為 MyApp 的已編譯資源檔：</span><span class="sxs-lookup"><span data-stu-id="c812c-106">The following example compiles MyApp.rc and creates a compiled resource file named MyApp.res in the same directory as MyApp.rc:</span></span>

<span data-ttu-id="c812c-107">**rc myapp .rc**</span><span class="sxs-lookup"><span data-stu-id="c812c-107">**rc myapp.rc**</span></span>

<span data-ttu-id="c812c-108">**/Fo** 選項提供產生的 .res 檔名稱，與對應 .rc 檔的名稱不同。</span><span class="sxs-lookup"><span data-stu-id="c812c-108">The **/fo** option gives the resulting .res file a name that differs from the name of the corresponding .rc file.</span></span> <span data-ttu-id="c812c-109">例如，若要將產生的 .res 檔 NewFile 命名為 .res，請使用下列命令：</span><span class="sxs-lookup"><span data-stu-id="c812c-109">For example, to name the resulting .res file NewFile.res, use the following command:</span></span>

<span data-ttu-id="c812c-110">**rc-fo 的 newfile myapp .rc**</span><span class="sxs-lookup"><span data-stu-id="c812c-110">**rc -fo newfile.res myapp.rc**</span></span>

<span data-ttu-id="c812c-111">**/Fo** 選項也可以將 .res 檔案放在不同的目錄中。</span><span class="sxs-lookup"><span data-stu-id="c812c-111">The **/fo** option can also place the .res file in a different directory.</span></span> <span data-ttu-id="c812c-112">例如，下列命令會將已編譯的資源檔 MyApp. .res 放置於目錄 C： \\ Source \\ 資源：</span><span class="sxs-lookup"><span data-stu-id="c812c-112">For example, the following command places the compiled resource file MyApp.res in the directory C:\\Source\\Resource:</span></span>

<span data-ttu-id="c812c-113">**rc-fo c： \\ 來源 \\ 資源 \\ myapp. .res myapp**</span><span class="sxs-lookup"><span data-stu-id="c812c-113">**rc -fo c:\\source\\resource\\myapp.res myapp.rc**</span></span>

 

 




