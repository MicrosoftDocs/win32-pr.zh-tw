---
title: 處理常式架構
description: 處理常式架構
ms.assetid: 93839b82-09cb-41af-ac0e-a8e9448bf04b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e2b02d0184d364ce438dc28f8219beea01c4868
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021550"
---
# <a name="handler-architecture"></a><span data-ttu-id="07b81-103">處理常式架構</span><span class="sxs-lookup"><span data-stu-id="07b81-103">Handler Architecture</span></span>

<span data-ttu-id="07b81-104">檔案或資料流程處理常式的內建函式是由處理常式本身定義。</span><span class="sxs-lookup"><span data-stu-id="07b81-104">The internal function of a file or stream handler is defined by the handler itself.</span></span> <span data-ttu-id="07b81-105">在應用程式中，檔案處理常式通常會以模組的形式出現，以讀取和寫入 AVI 檔。</span><span class="sxs-lookup"><span data-stu-id="07b81-105">To an application, a file handler typically appears as a module to read and write AVI files.</span></span> <span data-ttu-id="07b81-106">同樣地，資料流程處理常式會顯示為模組，以讀取和寫入特定類型的資料流程。</span><span class="sxs-lookup"><span data-stu-id="07b81-106">Similarly, a stream handler appears as a module to read and write a specific type of data stream.</span></span> <span data-ttu-id="07b81-107">一致的資料流程介面讓資料流程的來源和目的地對使用處理程式的應用程式不重要。</span><span class="sxs-lookup"><span data-stu-id="07b81-107">The consistent stream interface makes the source and destination of the stream unimportant to the application that uses the handler.</span></span>

<span data-ttu-id="07b81-108">檔案處理常式可存取包含一或多個資料流程的資料來源。</span><span class="sxs-lookup"><span data-stu-id="07b81-108">A file handler provides access to a data source consisting of one or more data streams.</span></span> <span data-ttu-id="07b81-109">檔案處理常式通常會提供存取包含一或多個資料流程的磁片檔案，而檔案處理常式的內部函式會讀取和寫入多媒體資料。</span><span class="sxs-lookup"><span data-stu-id="07b81-109">File handlers typically provide access to disk files containing one or more data streams, and the internal functions of the file handler read and write the multimedia data.</span></span> <span data-ttu-id="07b81-110">不過，檔案處理常式可以使用任何資料來源，例如包含數個混合資料流程的數位傳輸通道。</span><span class="sxs-lookup"><span data-stu-id="07b81-110">However, file handlers can work with any data source, such as a digital transmission channel containing several intermingled data streams.</span></span>

<span data-ttu-id="07b81-111">相反地，資料流程處理常式會處理一種資料類型，並顯示為應用程式的資料流程。</span><span class="sxs-lookup"><span data-stu-id="07b81-111">In contrast, a stream handler processes one type of data and appears as a data stream to an application.</span></span> <span data-ttu-id="07b81-112">資料流程處理常式可以提供其所產生的資料，或從檔案或外部來源取得資料。</span><span class="sxs-lookup"><span data-stu-id="07b81-112">A stream handler can provide data that it manufactures, or it can retrieve data from a file or an external source.</span></span> <span data-ttu-id="07b81-113">它會以您的應用程式可以使用的格式來提供其資料。</span><span class="sxs-lookup"><span data-stu-id="07b81-113">It supplies its data in a format that your application can use.</span></span>

 

 




