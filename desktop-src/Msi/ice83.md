---
description: ICE83 會驗證 MsiAssembly 資料表。
ms.assetid: dd290c73-6528-482d-8276-ac56d0fec181
title: ICE83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5ac38b4455875314c85fa08c1cfdc329e0cb470
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026635"
---
# <a name="ice83"></a><span data-ttu-id="1df5c-103">ICE83</span><span class="sxs-lookup"><span data-stu-id="1df5c-103">ICE83</span></span>

<span data-ttu-id="1df5c-104">ICE83 會驗證 [MsiAssembly 資料表](msiassembly-table.md)。</span><span class="sxs-lookup"><span data-stu-id="1df5c-104">ICE83 validates the [MsiAssembly table](msiassembly-table.md).</span></span> <span data-ttu-id="1df5c-105">如果包含 Win32 元件之元件的金鑰路徑設定為資訊清單檔，此 ICE 自訂動作會張貼錯誤。</span><span class="sxs-lookup"><span data-stu-id="1df5c-105">This ICE custom action posts an error if the key path for a component containing a Win32 assembly is set to the manifest file.</span></span> <span data-ttu-id="1df5c-106">如果在 [元件資料表](component-table.md) 的 [KeyPath] 欄位中輸入的值等於 [MsiAssembly] 資料表的 [檔案資訊清單] 欄位中輸入的值，就會明確地公佈錯誤 \_ 。</span><span class="sxs-lookup"><span data-stu-id="1df5c-106">Explicitly the error is posted if the value entered in the KeyPath field of the [Component table](component-table.md) equals the value entered in the File\_Manifest field of the MsiAssembly table.</span></span> <span data-ttu-id="1df5c-107">如果 MsiAssembly 資料表中至少有一筆記錄，而且 [InstallExecuteSequence 資料表](installexecutesequence-table.md) 不包含 [MsiPublishAssemblies 動作](msipublishassemblies-action.md) 和 [MSIUNPUBLISHASSEMBLIES 動作](msiunpublishassemblies-action.md)，則此 ICE 自訂動作會張貼錯誤。</span><span class="sxs-lookup"><span data-stu-id="1df5c-107">This ICE custom action posts an error if there is at least one record in the MsiAssembly table and the [InstallExecuteSequence table](installexecutesequence-table.md) does not contain both the [MsiPublishAssemblies Action](msipublishassemblies-action.md) and [MsiUnpublishAssemblies Action](msiunpublishassemblies-action.md).</span></span>

## <a name="result"></a><span data-ttu-id="1df5c-108">結果</span><span class="sxs-lookup"><span data-stu-id="1df5c-108">Result</span></span>

<span data-ttu-id="1df5c-109">ICE83 會張貼下列錯誤。</span><span class="sxs-lookup"><span data-stu-id="1df5c-109">ICE83 posts the following errors.</span></span>



| <span data-ttu-id="1df5c-110">ICE83 錯誤</span><span class="sxs-lookup"><span data-stu-id="1df5c-110">ICE83 error</span></span>                                                                                                   | <span data-ttu-id="1df5c-111">Description</span><span class="sxs-lookup"><span data-stu-id="1df5c-111">Description</span></span>                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1df5c-112">Win32 SXS 元件的金鑰路徑 (元件 \_ = \[ 1 \]) 不能是其資訊清單檔</span><span class="sxs-lookup"><span data-stu-id="1df5c-112">The key path for Win32 SXS Assembly (Component\_=\[1\]) SHOULD NOT be its manifest file</span></span>                       | <span data-ttu-id="1df5c-113">當 Win32 元件的 KeyPath 欄位設定為其資訊清單檔時，ICE83 會將此錯誤張貼 (元件。 KeyPath = = MsiAssembly。檔案 \_ 資訊清單) 。</span><span class="sxs-lookup"><span data-stu-id="1df5c-113">ICE83 posts this error when the KeyPath field for a Win32 Assembly is set to its manifest file (Component.KeyPath == MsiAssembly.File\_Manifest).</span></span> <span data-ttu-id="1df5c-114">\[1 \] 是元件資料表中的 KeyPath</span><span class="sxs-lookup"><span data-stu-id="1df5c-114">\[1\] is KeyPath in Component table</span></span>                          |
| <span data-ttu-id="1df5c-115">MsiPublishAssemblies 和 MsiUnpublishAssemblies 動作都必須存在於 InstallExecuteSequence 資料表中。</span><span class="sxs-lookup"><span data-stu-id="1df5c-115">Both MsiPublishAssemblies AND MsiUnpublishAssemblies actions MUST be present in InstallExecuteSequence table.</span></span> | <span data-ttu-id="1df5c-116">ICE83 會在 MsiAssembly 資料表中至少有一個專案時張貼此錯誤，但 InstallExecuteSequence 資料表不包含 MsiAssemblyPublish 動作和 MsiAssemblyUnpublish 動作。</span><span class="sxs-lookup"><span data-stu-id="1df5c-116">ICE83 posts this error when there is at least one entry in the MsiAssembly table but the InstallExecuteSequence table does not contain both the MsiAssemblyPublish action and the MsiAssemblyUnpublish action.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="1df5c-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="1df5c-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1df5c-118">ICE 參考</span><span class="sxs-lookup"><span data-stu-id="1df5c-118">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



