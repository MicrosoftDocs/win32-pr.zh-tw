---
description: 控制與 NTFS 檔案系統更新序號搭配使用的代碼和結構 (USN) 變更日誌。
ms.assetid: 2215f0d4-6ac8-42a5-87a5-9c76d1fae3ed
title: 變更日誌作業
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a52cda51d0efc4cbae1333fc197f42d6a5cc0f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988992"
---
# <a name="change-journal-operations"></a><span data-ttu-id="5e2bc-103">變更日誌作業</span><span class="sxs-lookup"><span data-stu-id="5e2bc-103">Change Journal Operations</span></span>

<span data-ttu-id="5e2bc-104">下列清單會識別使用 NTFS 檔案系統更新序號的控制程式代碼 (USN) 變更日誌。</span><span class="sxs-lookup"><span data-stu-id="5e2bc-104">The following list identifies the control codes that work with the NTFS file system update sequence number (USN) change journal.</span></span>

-   [<span data-ttu-id="5e2bc-105">**FSCTL \_ 建立 \_ USN \_ 日誌**</span><span class="sxs-lookup"><span data-stu-id="5e2bc-105">**FSCTL\_CREATE\_USN\_JOURNAL**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_create_usn_journal)
-   [<span data-ttu-id="5e2bc-106">**FSCTL \_ 刪除 \_ USN \_ 日誌**</span><span class="sxs-lookup"><span data-stu-id="5e2bc-106">**FSCTL\_DELETE\_USN\_JOURNAL**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_delete_usn_journal)
-   [<span data-ttu-id="5e2bc-107">**FSCTL \_ 列舉 \_ USN \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="5e2bc-107">**FSCTL\_ENUM\_USN\_DATA**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_enum_usn_data)
-   [<span data-ttu-id="5e2bc-108">**FSCTL \_ MARK \_ 把手**</span><span class="sxs-lookup"><span data-stu-id="5e2bc-108">**FSCTL\_MARK\_HANDLE**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_mark_handle)
-   [<span data-ttu-id="5e2bc-109">**FSCTL \_ 查詢 \_ USN \_ 日誌**</span><span class="sxs-lookup"><span data-stu-id="5e2bc-109">**FSCTL\_QUERY\_USN\_JOURNAL**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_usn_journal)
-   [<span data-ttu-id="5e2bc-110">**FSCTL \_ 讀取 \_ USN \_ 日誌**</span><span class="sxs-lookup"><span data-stu-id="5e2bc-110">**FSCTL\_READ\_USN\_JOURNAL**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_read_usn_journal)

<span data-ttu-id="5e2bc-111">下列清單會識別與 NTFS 檔案系統 USN 變更日誌相關的結構資訊。</span><span class="sxs-lookup"><span data-stu-id="5e2bc-111">The following list identifies the structures information that relates to the NTFS file system USN change journal.</span></span>

-   [<span data-ttu-id="5e2bc-112">**建立 \_ USN \_ 日誌 \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="5e2bc-112">**CREATE\_USN\_JOURNAL\_DATA**</span></span>](/windows/desktop/api/WinIoCtl/ns-winioctl-create_usn_journal_data)
-   [<span data-ttu-id="5e2bc-113">**刪除 \_ USN \_ 日誌 \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="5e2bc-113">**DELETE\_USN\_JOURNAL\_DATA**</span></span>](/windows/desktop/api/WinIoCtl/ns-winioctl-delete_usn_journal_data)
-   [<span data-ttu-id="5e2bc-114">**標記 \_ 控點 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="5e2bc-114">**MARK\_HANDLE\_INFO**</span></span>](/windows/desktop/api/WinIoCtl/ns-winioctl-mark_handle_info)
-   [<span data-ttu-id="5e2bc-115">**MFT \_ 列舉 \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="5e2bc-115">**MFT\_ENUM\_DATA**</span></span>](/windows/desktop/api/WinIoCtl/ns-winioctl-mft_enum_data_v0)
-   [<span data-ttu-id="5e2bc-116">**讀取 \_ USN \_ 日誌 \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="5e2bc-116">**READ\_USN\_JOURNAL\_DATA**</span></span>](/windows/desktop/api/WinIoCtl/ns-winioctl-read_usn_journal_data_v0)
-   [<span data-ttu-id="5e2bc-117">**USN \_ 日誌 \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="5e2bc-117">**USN\_JOURNAL\_DATA**</span></span>](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_journal_data_v0)
-   [<span data-ttu-id="5e2bc-118">**USN \_ 記錄**</span><span class="sxs-lookup"><span data-stu-id="5e2bc-118">**USN\_RECORD**</span></span>](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2)

 

 
