---
title: 註冊轉換外掛程式
description: 註冊轉換外掛程式
ms.assetid: d7d6e733-7288-4707-a54a-dcaa71601646
keywords:
- Windows Media Player，轉換外掛程式
- Windows Media Player 外掛程式，轉換
- 外掛程式，轉換
- 轉換外掛程式，註冊
- 登錄，轉換外掛程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 301d24e38cb4672936923cea9edd7fe6b3d2dc5c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106968631"
---
# <a name="registering-conversion-plug-ins"></a><span data-ttu-id="eec34-108">註冊轉換外掛程式</span><span class="sxs-lookup"><span data-stu-id="eec34-108">Registering Conversion Plug-ins</span></span>

<span data-ttu-id="eec34-109">必須先註冊協力廠商格式，Windows Media Player 才能具現化並使用轉換外掛程式。</span><span class="sxs-lookup"><span data-stu-id="eec34-109">Third-party formats must be registered before Windows Media Player can instantiate and use the conversion plug-in.</span></span> <span data-ttu-id="eec34-110">若要註冊您的檔案以進行轉換，您必須註冊與您的格式相關聯的副檔名。</span><span class="sxs-lookup"><span data-stu-id="eec34-110">To register your file for conversion, you must register the file name extension associated with your format.</span></span>

<span data-ttu-id="eec34-111">已註冊的副檔名清單會以一組登錄機碼的形式來保存。</span><span class="sxs-lookup"><span data-stu-id="eec34-111">The list of registered file name extensions is maintained as a set of registry keys.</span></span> <span data-ttu-id="eec34-112">如需註冊協力廠商格式的詳細資訊，請參閱副檔名登錄 [設定](file-name-extension-registry-settings.md)。</span><span class="sxs-lookup"><span data-stu-id="eec34-112">For details about registering third-party formats, see [File Name Extension Registry Settings](file-name-extension-registry-settings.md).</span></span> <span data-ttu-id="eec34-113">下表列出登錄值設定，以註冊協力廠商格式以使用轉換外掛程式進行轉換。</span><span class="sxs-lookup"><span data-stu-id="eec34-113">The following table lists the registry value settings to register a third-party format for conversion by using a conversion plug-in.</span></span>



| <span data-ttu-id="eec34-114">值</span><span class="sxs-lookup"><span data-stu-id="eec34-114">Value</span></span>                  | <span data-ttu-id="eec34-115">設定</span><span class="sxs-lookup"><span data-stu-id="eec34-115">Setting</span></span>                                                     |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="eec34-116">**執行階段**</span><span class="sxs-lookup"><span data-stu-id="eec34-116">**Runtime**</span></span>            | <span data-ttu-id="eec34-117">13</span><span class="sxs-lookup"><span data-stu-id="eec34-117">13</span></span>                                                          |
| <span data-ttu-id="eec34-118">**權限**</span><span class="sxs-lookup"><span data-stu-id="eec34-118">**Permissions**</span></span>        | <span data-ttu-id="eec34-119">8 (程式庫) 的許可權。</span><span class="sxs-lookup"><span data-stu-id="eec34-119">8 (Permission for the library).</span></span>                             |
| <span data-ttu-id="eec34-120">**ConvertPluginCLSID**</span><span class="sxs-lookup"><span data-stu-id="eec34-120">**ConvertPluginCLSID**</span></span> | <span data-ttu-id="eec34-121">轉換外掛程式的類別識別碼，以登錄格式為。</span><span class="sxs-lookup"><span data-stu-id="eec34-121">The class ID of the conversion plug-in, in registry format.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="eec34-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="eec34-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eec34-123">**轉換外掛程式程式設計參考**</span><span class="sxs-lookup"><span data-stu-id="eec34-123">**Conversion Plug-ins Programming Reference**</span></span>](conversion-plug-ins-programming-reference.md)
</dt> </dl>

 

 




