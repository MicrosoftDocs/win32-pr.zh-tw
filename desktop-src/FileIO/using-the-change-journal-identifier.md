---
description: NTFS 檔案系統會將不帶正負號的64位識別碼與每個變更日誌產生關聯。
ms.assetid: 5ae79460-b69a-4901-a417-1d5358dcba29
title: 使用變更日誌識別碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 692acf98403e45b6bdafd3cd4791a64dd1beb532
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106993038"
---
# <a name="using-the-change-journal-identifier"></a><span data-ttu-id="30eda-103">使用變更日誌識別碼</span><span class="sxs-lookup"><span data-stu-id="30eda-103">Using the Change Journal Identifier</span></span>

<span data-ttu-id="30eda-104">NTFS 檔案系統會將不帶正負號的64位識別碼與每個變更日誌產生關聯。</span><span class="sxs-lookup"><span data-stu-id="30eda-104">The NTFS file system associates an unsigned 64-bit identifier with each change journal.</span></span> <span data-ttu-id="30eda-105">建立時，會使用此識別碼來標記日誌。</span><span class="sxs-lookup"><span data-stu-id="30eda-105">The journal is stamped with this identifier when it is created.</span></span> <span data-ttu-id="30eda-106">檔案系統會使用新的識別碼來標記日誌，其中現有的更新序號 (USN) 記錄是或可能無法使用。</span><span class="sxs-lookup"><span data-stu-id="30eda-106">The file system stamps the journal with a new identifier where the existing update sequence number (USN) records either are or may be unusable.</span></span>

<span data-ttu-id="30eda-107">例如，當磁片區從某個 NTFS 版本移至另一個版本時，NTFS 檔案系統會以新的識別碼 restamps 變更日誌。</span><span class="sxs-lookup"><span data-stu-id="30eda-107">For example, the NTFS file system restamps a change journal with a new identifier when a volume is moved from one version of NTFS to another and then back.</span></span> <span data-ttu-id="30eda-108">這類移動可能會在雙重開機環境中發生，或在使用卸載式媒體時進行。</span><span class="sxs-lookup"><span data-stu-id="30eda-108">Such a move can happen in a dual-boot environment or when working with removable media.</span></span>

<span data-ttu-id="30eda-109">若要取得指定磁片區上目前變更日誌的識別碼，請使用 [**FSCTL \_ QUERY \_ USN \_ 日誌**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_usn_journal) 控制項程式碼。</span><span class="sxs-lookup"><span data-stu-id="30eda-109">To obtain the identifier of the current change journal on a specified volume, use the [**FSCTL\_QUERY\_USN\_JOURNAL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_usn_journal) control code.</span></span> <span data-ttu-id="30eda-110">若要執行此作業和所有其他變更日誌作業，您必須擁有系統管理員許可權。</span><span class="sxs-lookup"><span data-stu-id="30eda-110">To perform this and all other change journal operations, you must have system administrator privileges.</span></span> <span data-ttu-id="30eda-111">也就是說，您必須是 Administrators 群組的成員。</span><span class="sxs-lookup"><span data-stu-id="30eda-111">That is, you must be a member of the Administrators group.</span></span>

<span data-ttu-id="30eda-112">當系統管理員刪除並重新建立變更日誌時（例如，當目前的 USN 值接近最大可能的 USN 值）時，USN 值會從零開始。</span><span class="sxs-lookup"><span data-stu-id="30eda-112">When an administrator deletes and re-creates the change journal, for example when the current USN value approaches the maximum possible USN value, the USN values begin again from zero.</span></span> <span data-ttu-id="30eda-113">當 NTFS 檔案系統使用新的識別碼來標記日誌，而不是重新建立日誌時，它不會將 USN 重設為零，但會從目前的 USN 繼續。</span><span class="sxs-lookup"><span data-stu-id="30eda-113">When the NTFS file system stamps a journal with a new identifier rather than re-creating the journal, it does not reset the USN to zero but continues from the current USN.</span></span> <span data-ttu-id="30eda-114">無論是哪一種情況，所有現有的 Usn 都小於未來的 Usn。</span><span class="sxs-lookup"><span data-stu-id="30eda-114">In either case, all existing USNs are less than any future USNs.</span></span>

<span data-ttu-id="30eda-115">當您需要一組特定記錄的資訊時，請使用 [**FSCTL \_ 查詢 \_ USN \_ 日誌**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_usn_journal) 控制程式代碼來取得變更日誌識別碼。</span><span class="sxs-lookup"><span data-stu-id="30eda-115">When you need information on a specific set of records, use the [**FSCTL\_QUERY\_USN\_JOURNAL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_usn_journal) control code to obtain the change journal identifier.</span></span> <span data-ttu-id="30eda-116">然後使用 [**FSCTL \_ 讀取 \_ USN \_ 日誌**](/windows/win32/api/winioctl/ni-winioctl-fsctl_read_usn_journal) 控制程式代碼來讀取感興趣的日誌記錄。</span><span class="sxs-lookup"><span data-stu-id="30eda-116">Then use the [**FSCTL\_READ\_USN\_JOURNAL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_read_usn_journal) control code to read the journal records of interest.</span></span> <span data-ttu-id="30eda-117">NTFS 檔案系統只會傳回識別碼所指定之日誌的有效記錄。</span><span class="sxs-lookup"><span data-stu-id="30eda-117">The NTFS file system only returns records that are valid for the journal specified by the identifier.</span></span>

<span data-ttu-id="30eda-118">您的應用程式需要記錄的 Usn 和識別碼來讀取日誌。</span><span class="sxs-lookup"><span data-stu-id="30eda-118">Your application needs both the records' USNs and the identifier to read the journal.</span></span> <span data-ttu-id="30eda-119">如果您的應用程式應該忽略檔案中的現有記錄，且記錄是針對相同磁片區在日誌的先前實例中寫入，則這項需求會提供完整性檢查。</span><span class="sxs-lookup"><span data-stu-id="30eda-119">This requirement provides an integrity check for cases where your application should ignore the existing records in the file and where records were written in previous instances of the journal for the same volume.</span></span>

<span data-ttu-id="30eda-120">若要取得您感興趣的記錄，您必須從最舊的記錄開始 (也就是最低的 USN) 並向前掃描，直到您找到感興趣的第一筆記錄為止。</span><span class="sxs-lookup"><span data-stu-id="30eda-120">To obtain the records in which you are interested, you must start at the oldest record (that is, with the lowest USN) and scan forward until you locate the first record of interest.</span></span>

 

 
