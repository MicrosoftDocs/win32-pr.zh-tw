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
# <a name="ms-dos-date-and-time"></a>MS-DOS 日期和時間

**Ms-dos 日期** 和 **ms-dos 時間** 是封裝的16位值，可指定最後寫入 MS-DOS 檔案的月份、日期、年份和時間。 MS-DOS 會記錄每次 MS-DOS 應用程式建立或寫入檔案時的日期和時間。 MS-DOS 應用程式會使用 MS-DOS 函式來取得此日期和時間。 當您使用 [**GetFileTime**](/windows/desktop/api/FileAPI/nf-fileapi-getfiletime) 函式來抓取 ms-dos 所建立之檔案的檔案時間時， **GetFileTime** 會自動將 ms-dos 日期和時間轉換成 UTC 時間。

如果您遇到尚未轉換的 MS-DOS 日期和時間，您可以使用 [**DosDateTimeToFileTime**](/windows/desktop/api/Winbase/nf-winbase-dosdatetimetofiletime) 函數將它轉換成 UTC 時間。 此函數會將轉換後的日期和時間複製到 [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) 結構。 您可以使用 [**FileTimeToDosDateTime**](/windows/desktop/api/Winbase/nf-winbase-filetimetodosdatetime) 函數，將值轉換回 MS-DOS 日期和時間。

 

 
