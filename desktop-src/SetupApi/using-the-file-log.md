---
description: 在您可以使用檔案記錄檔之前，必須先呼叫 SetupInitializeFileLog 來開啟或建立檔案記錄檔。 當您呼叫此函式時，您可以指定旗標來建立或覆寫檔案記錄檔、開啟系統記錄檔，或以唯讀方式開啟檔案記錄檔。
ms.assetid: 7ab133f6-2088-4bca-bf24-d3dcb29376a1
title: 使用檔案記錄檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf7f1e3d27ba7d42d448a1eac48d60246c2b40db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945494"
---
# <a name="using-the-file-log"></a><span data-ttu-id="3d737-104">使用檔案記錄檔</span><span class="sxs-lookup"><span data-stu-id="3d737-104">Using the File Log</span></span>

<span data-ttu-id="3d737-105">在您可以使用檔案記錄檔之前，必須先呼叫 [**SetupInitializeFileLog**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitializefileloga) 來開啟或建立檔案記錄檔。</span><span class="sxs-lookup"><span data-stu-id="3d737-105">Before you can use a file log, you must call [**SetupInitializeFileLog**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitializefileloga) to open or create it.</span></span> <span data-ttu-id="3d737-106">當您呼叫此函式時，您可以指定旗標來建立或覆寫檔案記錄檔、開啟系統記錄檔，或以唯讀方式開啟檔案記錄檔。</span><span class="sxs-lookup"><span data-stu-id="3d737-106">When you call this function, you can specify flags to create or overwrite a file log, open the system log, or open a file log as read-only.</span></span>

<span data-ttu-id="3d737-107">在 [**SetupInitializeFileLog**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitializefileloga) 將控制碼傳回至檔案記錄檔之後，您可以藉由呼叫 [**SetupLogFile**](/windows/desktop/api/Setupapi/nf-setupapi-setuplogfilea)來加入專案、藉由呼叫 [**SetupRemoveFileLogEntry**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovefilelogentrya)來刪除專案，或是藉由呼叫 [**SetupQueryFileLog**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryfileloga)來取得檔案記錄檔中特定檔案的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="3d737-107">After [**SetupInitializeFileLog**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitializefileloga) returns a handle to a file log, you can add an entry by calling [**SetupLogFile**](/windows/desktop/api/Setupapi/nf-setupapi-setuplogfilea), delete an entry by calling [**SetupRemoveFileLogEntry**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovefilelogentrya), or retrieve information about a particular file in a file log by calling [**SetupQueryFileLog**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryfileloga).</span></span>

<span data-ttu-id="3d737-108">當不再需要檔案記錄檔時，應呼叫 [**SetupTerminateFileLog**](/windows/desktop/api/Setupapi/nf-setupapi-setupterminatefilelog) 來釋放在呼叫 [**SetupInitializeFileLog**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitializefileloga)時所配置的資源。</span><span class="sxs-lookup"><span data-stu-id="3d737-108">When the file log is no longer needed, [**SetupTerminateFileLog**](/windows/desktop/api/Setupapi/nf-setupapi-setupterminatefilelog) should be called to release the resources allocated during the call to [**SetupInitializeFileLog**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitializefileloga).</span></span>

 

 



