---
description: ICE53 會檢查登錄表中的專案，以將私人安裝程式資訊或原則值寫入系統登錄。
ms.assetid: f5afca1f-bd36-4f95-a62a-f6b2e37238a6
title: ICE53
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c323a502642e3cf5999e6cb332a434a9fc8a41db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106995860"
---
# <a name="ice53"></a><span data-ttu-id="90fe1-103">ICE53</span><span class="sxs-lookup"><span data-stu-id="90fe1-103">ICE53</span></span>

<span data-ttu-id="90fe1-104">ICE53 會檢查登錄表中的專案，以將私人安裝程式資訊或原則值寫入系統登錄。</span><span class="sxs-lookup"><span data-stu-id="90fe1-104">ICE53 checks for entries in the Registry table that write private installer information or policy values to the system registry.</span></span>

## <a name="result"></a><span data-ttu-id="90fe1-105">結果</span><span class="sxs-lookup"><span data-stu-id="90fe1-105">Result</span></span>

<span data-ttu-id="90fe1-106">如果登錄資料表指定將內部或原則資訊寫入登錄，ICE53 會張貼警告。</span><span class="sxs-lookup"><span data-stu-id="90fe1-106">ICE53 posts a warning if the Registry table specifies writing internal or policy information to the registry.</span></span>

## <a name="example"></a><span data-ttu-id="90fe1-107">範例</span><span class="sxs-lookup"><span data-stu-id="90fe1-107">Example</span></span>

<span data-ttu-id="90fe1-108">ICE53 會針對所顯示的範例張貼下列警告。</span><span class="sxs-lookup"><span data-stu-id="90fe1-108">ICE53 posts the following warning for the example shown.</span></span>

``` syntax
Registry Key 'Registry1' writes Installer internal or policy information.
```

<span data-ttu-id="90fe1-109">登錄[表](registry-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="90fe1-109">[Registry Table](registry-table.md) (partial)</span></span>



| <span data-ttu-id="90fe1-110">登錄</span><span class="sxs-lookup"><span data-stu-id="90fe1-110">Registry</span></span>             | <span data-ttu-id="90fe1-111">Root</span><span class="sxs-lookup"><span data-stu-id="90fe1-111">Root</span></span>         | <span data-ttu-id="90fe1-112">答案</span><span class="sxs-lookup"><span data-stu-id="90fe1-112">Key</span></span>                                                                                                   |
|----------------------|--------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90fe1-113">Registry1</span><span class="sxs-lookup"><span data-stu-id="90fe1-113">Registry1</span></span><br/> | <span data-ttu-id="90fe1-114">1</span><span class="sxs-lookup"><span data-stu-id="90fe1-114">1</span></span><br/> | <span data-ttu-id="90fe1-115">**軟體** \\**原則** \\**Microsoft** \\**Windows** \\**安裝程式** \\**DisableRollback**</span><span class="sxs-lookup"><span data-stu-id="90fe1-115">**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**\\**DisableRollback**</span></span><br/> |



 

<span data-ttu-id="90fe1-116">登錄資料表資料列 ' Registry1 ' 會寫入登錄中的系統原則值，以影響所有封裝的安裝。</span><span class="sxs-lookup"><span data-stu-id="90fe1-116">Registry table row 'Registry1' writes a system policy value in the registry that affects the installation of all packages.</span></span> <span data-ttu-id="90fe1-117">根據封裝，您可以藉由在 [屬性工作表](property-table.md)中設定 [**DISABLEROLLBACK**](-disablerollback.md)屬性，來停用此封裝的復原。</span><span class="sxs-lookup"><span data-stu-id="90fe1-117">Depending on the package, it may be possible to disable rollback for this package alone by setting the [**DISABLEROLLBACK**](-disablerollback.md) property in the [Property table](property-table.md).</span></span> <span data-ttu-id="90fe1-118">請參閱 [復原安裝](rollback-installation.md)。</span><span class="sxs-lookup"><span data-stu-id="90fe1-118">See [Rollback Installation](rollback-installation.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="90fe1-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="90fe1-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="90fe1-120">ICE 參考</span><span class="sxs-lookup"><span data-stu-id="90fe1-120">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 




