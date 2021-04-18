---
description: MS-DOS 日期和 MS-DOS 時間是封裝的16位值，可指定最後寫入 MS-DOS 檔案的月份、日期、年份和時間。
ms.assetid: 948e6d77-dd01-4c90-9ef0-af143972c3fa
title: MS-DOS 日期和時間
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84d401c731c9a3f5127511e28adf846c929a89a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971445"
---
# <a name="ms-dos-date-and-time"></a><span data-ttu-id="7a0fa-103">MS-DOS 日期和時間</span><span class="sxs-lookup"><span data-stu-id="7a0fa-103">MS-DOS Date and Time</span></span>

<span data-ttu-id="7a0fa-104">**Ms-dos 日期** 和 **ms-dos 時間** 是封裝的16位值，可指定最後寫入 MS-DOS 檔案的月份、日期、年份和時間。</span><span class="sxs-lookup"><span data-stu-id="7a0fa-104">**MS-DOS date** and **MS-DOS time** are packed 16-bit values that specify the month, day, year, and time of day an MS-DOS file was last written to.</span></span> <span data-ttu-id="7a0fa-105">MS-DOS 會記錄每次 MS-DOS 應用程式建立或寫入檔案時的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="7a0fa-105">MS-DOS records the date and time whenever an MS-DOS application creates or writes to a file.</span></span> <span data-ttu-id="7a0fa-106">MS-DOS 應用程式會使用 MS-DOS 函式來取得此日期和時間。</span><span class="sxs-lookup"><span data-stu-id="7a0fa-106">MS-DOS applications retrieve this date and time using MS-DOS functions.</span></span> <span data-ttu-id="7a0fa-107">當您使用 [**GetFileTime**](/windows/desktop/api/FileAPI/nf-fileapi-getfiletime) 函式來抓取 ms-dos 所建立之檔案的檔案時間時， **GetFileTime** 會自動將 ms-dos 日期和時間轉換成 UTC 時間。</span><span class="sxs-lookup"><span data-stu-id="7a0fa-107">When you use the [**GetFileTime**](/windows/desktop/api/FileAPI/nf-fileapi-getfiletime) function to retrieve the file times for files that were created by MS-DOS, **GetFileTime** automatically converts MS-DOS dates and times to UTC-based times.</span></span>

<span data-ttu-id="7a0fa-108">如果您遇到尚未轉換的 MS-DOS 日期和時間，您可以使用 [**DosDateTimeToFileTime**](/windows/desktop/api/Winbase/nf-winbase-dosdatetimetofiletime) 函數將它轉換成 UTC 時間。</span><span class="sxs-lookup"><span data-stu-id="7a0fa-108">If you encounter an MS-DOS date and time that has not been converted, you can convert it to a UTC-based time by using the [**DosDateTimeToFileTime**](/windows/desktop/api/Winbase/nf-winbase-dosdatetimetofiletime) function.</span></span> <span data-ttu-id="7a0fa-109">此函數會將轉換後的日期和時間複製到 [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) 結構。</span><span class="sxs-lookup"><span data-stu-id="7a0fa-109">This function copies the converted date and time to a [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) structure.</span></span> <span data-ttu-id="7a0fa-110">您可以使用 [**FileTimeToDosDateTime**](/windows/desktop/api/Winbase/nf-winbase-filetimetodosdatetime) 函數，將值轉換回 MS-DOS 日期和時間。</span><span class="sxs-lookup"><span data-stu-id="7a0fa-110">You can convert the value back to an MS-DOS date and time by using the [**FileTimeToDosDateTime**](/windows/desktop/api/Winbase/nf-winbase-filetimetodosdatetime) function.</span></span>

 

 
