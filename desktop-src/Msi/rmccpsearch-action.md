---
description: RMCCPSearch 動作會在執行升級安裝之前，使用檔案簽章來驗證是否已在系統上安裝合格產品。
ms.assetid: d37b2434-86eb-4c6e-b817-77c75dcebbf5
title: RMCCPSearch 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c273ccb03bb77e0346edf73177d938d6002878a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106981478"
---
# <a name="rmccpsearch-action"></a><span data-ttu-id="548f4-103">RMCCPSearch 動作</span><span class="sxs-lookup"><span data-stu-id="548f4-103">RMCCPSearch Action</span></span>

<span data-ttu-id="548f4-104">RMCCPSearch 動作會在執行升級安裝之前，使用檔案簽章來驗證是否已在系統上安裝合格產品。</span><span class="sxs-lookup"><span data-stu-id="548f4-104">The RMCCPSearch action uses file signatures to validate that qualifying products are installed on a system before an upgrade installation is performed.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="548f4-105">順序限制</span><span class="sxs-lookup"><span data-stu-id="548f4-105">Sequence Restrictions</span></span>

<span data-ttu-id="548f4-106">RMCCPSearch 動作應該撰寫到 [InstallUISequence 資料表](installuisequence-table.md) 和 [InstallExecuteSequence 資料表](installexecutesequence-table.md)中。</span><span class="sxs-lookup"><span data-stu-id="548f4-106">RMCCPSearch action should be authored into the [InstallUISequence table](installuisequence-table.md) and [InstallExecuteSequence table](installexecutesequence-table.md).</span></span> <span data-ttu-id="548f4-107">如果動作已在 InstallUISequence 序列中執行，則安裝程式會防止 RMCCPSearch 在 InstallExecuteSequence 序列中執行。</span><span class="sxs-lookup"><span data-stu-id="548f4-107">The installer prevents RMCCPSearch from running in the InstallExecuteSequence sequence if the action has already run in InstallUISequence sequence.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="548f4-108">ActionData 訊息</span><span class="sxs-lookup"><span data-stu-id="548f4-108">ActionData Messages</span></span>

<span data-ttu-id="548f4-109">沒有任何 ActionData 訊息。</span><span class="sxs-lookup"><span data-stu-id="548f4-109">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="548f4-110">備註</span><span class="sxs-lookup"><span data-stu-id="548f4-110">Remarks</span></span>

<span data-ttu-id="548f4-111">RMCCPSearch 動作要求 [**CCP \_ 磁片磁碟機**](ccp-drive.md) 屬性必須設定為卸載式 [*磁片*](v-gly.md) 區上的根路徑，該磁片區具有任何合格產品的安裝。</span><span class="sxs-lookup"><span data-stu-id="548f4-111">The RMCCPSearch action requires the [**CCP\_DRIVE**](ccp-drive.md) property to be set to the root path on the removable [*volume*](v-gly.md) that has the installation for any of the qualifying products.</span></span>

<span data-ttu-id="548f4-112">在使用 [DrLocator](drlocator-table.md)資料表之 [**CCP \_ 磁片磁碟機**](ccp-drive.md)屬性所參考的路徑下，搜尋 CCPSearch 資料表中的每個檔案簽章。</span><span class="sxs-lookup"><span data-stu-id="548f4-112">Each file signature in the CCPSearch table is searched for under the path referred to by the [**CCP\_DRIVE**](ccp-drive.md) property using the [DrLocator](drlocator-table.md) table.</span></span> <span data-ttu-id="548f4-113">簽 [章資料表缺少](signature-table.md) 簽章代表目錄。</span><span class="sxs-lookup"><span data-stu-id="548f4-113">The absence of the signature from the [Signature](signature-table.md) table denotes a directory.</span></span> <span data-ttu-id="548f4-114">如果有任何簽章確定存在，RMCCPSearch 動作就會終止。</span><span class="sxs-lookup"><span data-stu-id="548f4-114">If any signature is determined to exist, the RMCCPSearch action terminates.</span></span>

## <a name="related-topics"></a><span data-ttu-id="548f4-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="548f4-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="548f4-116">CCPSearch 資料表</span><span class="sxs-lookup"><span data-stu-id="548f4-116">CCPSearch table</span></span>](ccpsearch-table.md)
</dt> </dl>

 

 



