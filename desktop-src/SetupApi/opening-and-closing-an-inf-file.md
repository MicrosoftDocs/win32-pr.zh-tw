---
description: 在設定函數可以存取 INF 中的資訊之前，您必須使用 SetupOpenInfFile 函式的呼叫來開啟它。 此函數會傳回 INF 檔案的控制碼。
ms.assetid: d838c05c-51e4-49a8-b773-af4924bff7e2
title: 開啟和關閉 INF 檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 893b72d000f433fb4da7ecfee0db4d856f878814
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104513544"
---
# <a name="opening-and-closing-an-inf-file"></a><span data-ttu-id="a72cd-104">開啟和關閉 INF 檔案</span><span class="sxs-lookup"><span data-stu-id="a72cd-104">Opening and Closing an INF file</span></span>

<span data-ttu-id="a72cd-105">在設定函數可以存取 INF 中的資訊之前，您必須使用 [**SetupOpenInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopeninffilea) 函式的呼叫來開啟它。</span><span class="sxs-lookup"><span data-stu-id="a72cd-105">Before the setup functions can access information in the INF, you must open it with a call to the [**SetupOpenInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopeninffilea) function.</span></span> <span data-ttu-id="a72cd-106">此函數會傳回 INF 檔案的控制碼。</span><span class="sxs-lookup"><span data-stu-id="a72cd-106">This function returns a handle to the INF file.</span></span>

<span data-ttu-id="a72cd-107">如果您不知道需要開啟的 INF 檔案名，可以使用 [**SetupGetInfFileList**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetinffilelista) 函式來取得目錄中的 inf 檔案清單。</span><span class="sxs-lookup"><span data-stu-id="a72cd-107">If you do not know the name of the INF file that you need to open, you can use the [**SetupGetInfFileList**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetinffilelista) function to obtain a list of INF files in a directory.</span></span>

<span data-ttu-id="a72cd-108">開啟 INF 檔案之後，您可以使用 [**SetupOpenAppendInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea) 函式，將其他 INF 檔案附加至已開啟的 inf 檔案。</span><span class="sxs-lookup"><span data-stu-id="a72cd-108">After you open an INF file, you can append additional INF files to the opened INF file by using the [**SetupOpenAppendInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea) function.</span></span> <span data-ttu-id="a72cd-109">這項功能類似于 include 語句。</span><span class="sxs-lookup"><span data-stu-id="a72cd-109">This is functionally similar to an include statement.</span></span> <span data-ttu-id="a72cd-110">當後續安裝函式參考開放式 INF 檔案時，也可以存取儲存在附加檔案中的任何資訊。</span><span class="sxs-lookup"><span data-stu-id="a72cd-110">When subsequent setup functions reference an open INF file, they will also be able to access any information stored in the appended files.</span></span>

<span data-ttu-id="a72cd-111">如果您未在 [**SetupOpenAppendInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea)函式的呼叫期間指定 INF 檔案， **SetupOpenAppendInfFile** 會在 open INF 檔案的 [**版本**] 區段中，將 **LayoutFile** 金鑰所指定的)  (的檔案附加至該檔案。</span><span class="sxs-lookup"><span data-stu-id="a72cd-111">If you do not specify an INF file during the call to the [**SetupOpenAppendInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea) function, **SetupOpenAppendInfFile** appends the file(s) specified by the **LayoutFile** key in the **Version** section of the open INF file.</span></span>

<span data-ttu-id="a72cd-112">當您不再需要 INF 檔案中的資訊時，請呼叫 [**SetupCloseInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupcloseinffile) 函式釋放在呼叫 [**SetupOpenAppendInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea)期間所配置的資源。</span><span class="sxs-lookup"><span data-stu-id="a72cd-112">When you no longer need the information in the INF file, call the [**SetupCloseInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupcloseinffile) function to release resources allocated during the call to [**SetupOpenAppendInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea).</span></span>

 

 



