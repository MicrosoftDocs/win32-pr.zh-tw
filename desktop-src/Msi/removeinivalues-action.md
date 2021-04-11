---
description: 如果元件設定為在本機安裝或從來源執行，則 RemoveIniValues 動作會移除在 RemoveIniFile 資料表中指定要移除的 .ini 檔案資訊。
ms.assetid: a30793c8-4154-4990-a42a-d022e69f960a
title: RemoveIniValues 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7dfb847d911e847de00ede6eab30ac3a86615eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945253"
---
# <a name="removeinivalues-action"></a><span data-ttu-id="c53cc-103">RemoveIniValues 動作</span><span class="sxs-lookup"><span data-stu-id="c53cc-103">RemoveIniValues Action</span></span>

<span data-ttu-id="c53cc-104">如果元件設定為在本機安裝或從來源執行，則 RemoveIniValues 動作會移除在 [RemoveIniFile 資料表](removeinifile-table.md) 中指定要移除的 .ini 檔案資訊。</span><span class="sxs-lookup"><span data-stu-id="c53cc-104">The RemoveIniValues action removes .ini file information specified for removal in the [RemoveIniFile table](removeinifile-table.md) if the component is set to be installed locally or run-from-source.</span></span> <span data-ttu-id="c53cc-105">RemoveIniValues 動作會移除與 [IniFile 資料表](inifile-table.md)中的元件相關聯的 .ini 檔案資訊。</span><span class="sxs-lookup"><span data-stu-id="c53cc-105">The RemoveIniValues action removes .ini file information that has been associated with a component in the [IniFile table](inifile-table.md).</span></span> <span data-ttu-id="c53cc-106">如果資訊是由 [WriteIniValues 動作](writeinivalues-action.md) 寫入，而元件已排程要卸載，此動作也會移除 .ini 檔案資訊。</span><span class="sxs-lookup"><span data-stu-id="c53cc-106">This action also removes .ini file information if the information was written by the [WriteIniValues action](writeinivalues-action.md) and the component is scheduled to be uninstalled.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="c53cc-107">順序限制</span><span class="sxs-lookup"><span data-stu-id="c53cc-107">Sequence Restrictions</span></span>

<span data-ttu-id="c53cc-108">[InstallValidate](installvalidate-action.md)動作必須在 RemoveIniValues 動作之前呼叫。</span><span class="sxs-lookup"><span data-stu-id="c53cc-108">The [InstallValidate](installvalidate-action.md) action must be called before the RemoveIniValues action.</span></span> <span data-ttu-id="c53cc-109">如果序列中使用 [WriteIniValues](writeinivalues-action.md) 動作，它必須出現在 RemoveIniValues 之後。</span><span class="sxs-lookup"><span data-stu-id="c53cc-109">If a [WriteIniValues](writeinivalues-action.md) action is used in the sequence, it must appear after RemoveIniValues.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="c53cc-110">ActionData 訊息</span><span class="sxs-lookup"><span data-stu-id="c53cc-110">ActionData Messages</span></span>



| <span data-ttu-id="c53cc-111">欄位</span><span class="sxs-lookup"><span data-stu-id="c53cc-111">Field</span></span> | <span data-ttu-id="c53cc-112">動作資料的描述</span><span class="sxs-lookup"><span data-stu-id="c53cc-112">Description of action data</span></span>    |
|-------|-------------------------------|
| <span data-ttu-id="c53cc-113">\[1\]</span><span class="sxs-lookup"><span data-stu-id="c53cc-113">\[1\]</span></span> | <span data-ttu-id="c53cc-114">.Ini 檔案的識別碼。</span><span class="sxs-lookup"><span data-stu-id="c53cc-114">Identifier of .ini file.</span></span>      |
| <span data-ttu-id="c53cc-115">\[2\]</span><span class="sxs-lookup"><span data-stu-id="c53cc-115">\[2\]</span></span> | <span data-ttu-id="c53cc-116">.Ini 檔案金鑰區段。</span><span class="sxs-lookup"><span data-stu-id="c53cc-116">An .ini file key section.</span></span>     |
| <span data-ttu-id="c53cc-117">\[3\]</span><span class="sxs-lookup"><span data-stu-id="c53cc-117">\[3\]</span></span> | <span data-ttu-id="c53cc-118">從 .ini 檔案移除的專案。</span><span class="sxs-lookup"><span data-stu-id="c53cc-118">Item removed from .ini file.</span></span>  |
| <span data-ttu-id="c53cc-119">\[4\]</span><span class="sxs-lookup"><span data-stu-id="c53cc-119">\[4\]</span></span> | <span data-ttu-id="c53cc-120">從 .ini 檔案中移除的值。</span><span class="sxs-lookup"><span data-stu-id="c53cc-120">Value removed from .ini file.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="c53cc-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="c53cc-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c53cc-122">RemoveIniFile 資料表</span><span class="sxs-lookup"><span data-stu-id="c53cc-122">RemoveIniFile table</span></span>](removeinifile-table.md)
</dt> <dt>

[<span data-ttu-id="c53cc-123">IniFile 資料表</span><span class="sxs-lookup"><span data-stu-id="c53cc-123">IniFile table</span></span>](inifile-table.md)
</dt> <dt>

[<span data-ttu-id="c53cc-124">WriteIniValues 動作</span><span class="sxs-lookup"><span data-stu-id="c53cc-124">WriteIniValues action</span></span>](writeinivalues-action.md)
</dt> <dt>

[<span data-ttu-id="c53cc-125">InstallValidate</span><span class="sxs-lookup"><span data-stu-id="c53cc-125">InstallValidate</span></span>](installvalidate-action.md)
</dt> </dl>

 

 



