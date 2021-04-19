---
description: 若要取得磁片區的控制碼以用於更新序號 (USN) 變更日誌作業，請呼叫 CreateFile 函式，並將 lpFileName 參數設定為下列格式的字串： \\ \\ 。 \\X。
ms.assetid: a4f4dac5-76fd-4e9e-a71e-665684840d74
title: 取得變更日誌作業的磁片區控制碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8036fc642de52aa2d7f9bab66dd2e380dcc070c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987820"
---
# <a name="obtaining-a-volume-handle-for-change-journal-operations"></a><span data-ttu-id="01fd5-103">取得變更日誌作業的磁片區控制碼</span><span class="sxs-lookup"><span data-stu-id="01fd5-103">Obtaining a Volume Handle for Change Journal Operations</span></span>

<span data-ttu-id="01fd5-104">若要取得磁片區的控制碼以用於更新序號 (USN) 變更日誌作業，請呼叫 [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)函式，並將 *lpFileName* 參數設定為下列格式的字串： \\ \\ 。 \\*X*：</span><span class="sxs-lookup"><span data-stu-id="01fd5-104">To obtain a handle to a volume for use with update sequence number (USN) change journal operations, call the [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) function with the *lpFileName* parameter set to a string of the following form: \\\\.\\*X*:</span></span>

<span data-ttu-id="01fd5-105">請注意， *X* 是識別 NTFS 磁片區出現所在磁片磁碟機的字母。</span><span class="sxs-lookup"><span data-stu-id="01fd5-105">Note that *X* is the letter that identifies the drive on which the NTFS volume appears.</span></span>

<span data-ttu-id="01fd5-106">如果磁片區沒有磁碟機號，請使用 [命名磁片](naming-a-volume.md)區中所述的語法。</span><span class="sxs-lookup"><span data-stu-id="01fd5-106">If the volume does not have a drive letter, use the syntax described in [Naming a Volume](naming-a-volume.md).</span></span>

 

 



