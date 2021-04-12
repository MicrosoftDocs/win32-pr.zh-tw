---
description: 您必須註冊您的辨識器 DLL，才能使用它的 Tablet PC 平臺。 辨識器必須在安裝時對登錄進行下列變更。
ms.assetid: 1f1d826b-3968-424b-8da8-b69590058ff1
title: 註冊您的辨識器 DLL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51114f11868e6d45dc4d319dab60e5b4f094ddbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104514177"
---
# <a name="registering-your-recognizer-dll"></a><span data-ttu-id="cccf6-104">註冊您的辨識器 DLL</span><span class="sxs-lookup"><span data-stu-id="cccf6-104">Registering Your Recognizer DLL</span></span>

<span data-ttu-id="cccf6-105">您必須註冊您的辨識器 DLL，才能使用它的 Tablet PC 平臺。</span><span class="sxs-lookup"><span data-stu-id="cccf6-105">Your recognizer DLL must be registered for the Tablet PC Platform to use it.</span></span> <span data-ttu-id="cccf6-106">辨識器必須在安裝時對登錄進行下列變更。</span><span class="sxs-lookup"><span data-stu-id="cccf6-106">The recognizer must make the following changes to the registry at installation.</span></span>

<span data-ttu-id="cccf6-107">在 HKEY \_ LOCAL \_ MACHINE/SOFTWARE/MICROSOFT/TPG/辨識器/登錄機碼下，為您的辨識器的每個 clsid 新增金鑰。</span><span class="sxs-lookup"><span data-stu-id="cccf6-107">Add a new key for each of the CLSIDs of your recognizer under the HKEY\_LOCAL\_MACHINE/SOFTWARE/Microsoft/TPG/Recognizers/ registry key.</span></span> <span data-ttu-id="cccf6-108">為每種語言新增一個 CLSID。</span><span class="sxs-lookup"><span data-stu-id="cccf6-108">Add one CLSID per language.</span></span> <span data-ttu-id="cccf6-109">下表描述每個包含 Clsid 的索引鍵下應新增的值。</span><span class="sxs-lookup"><span data-stu-id="cccf6-109">The following table describes the values that should be added underneath each of the keys containing your CLSIDs.</span></span>

> [!Note]  
> <span data-ttu-id="cccf6-110">這些值的名稱會區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="cccf6-110">The names of these values are case sensitive.</span></span>

 



| <span data-ttu-id="cccf6-111">值名稱</span><span class="sxs-lookup"><span data-stu-id="cccf6-111">Value name</span></span>                             | <span data-ttu-id="cccf6-112">值類型</span><span class="sxs-lookup"><span data-stu-id="cccf6-112">Value type</span></span>             | <span data-ttu-id="cccf6-113">值說明</span><span class="sxs-lookup"><span data-stu-id="cccf6-113">Value description</span></span>                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------------------------------|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cccf6-114">辨識器功能旗標</span><span class="sxs-lookup"><span data-stu-id="cccf6-114">Recognizer Capability Flags</span></span><br/> | <span data-ttu-id="cccf6-115">REG \_ DWORD</span><span class="sxs-lookup"><span data-stu-id="cccf6-115">REG\_DWORD</span></span><br/>  | <span data-ttu-id="cccf6-116">用來判斷辨識器功能的 DWORD。</span><span class="sxs-lookup"><span data-stu-id="cccf6-116">DWORD used to determine the capabilities of the recognizer.</span></span><br/>                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="cccf6-117">辨識器 DLL</span><span class="sxs-lookup"><span data-stu-id="cccf6-117">Recognizer DLL</span></span><br/>              | <span data-ttu-id="cccf6-118">REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="cccf6-118">REG\_SZ</span></span><br/>     | <span data-ttu-id="cccf6-119">已安裝的辨識器 DLL 的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="cccf6-119">Full path to the installed recognizer DLL.</span></span><br/>                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="cccf6-120">辨識的語言</span><span class="sxs-lookup"><span data-stu-id="cccf6-120">Recognized Languages</span></span><br/>        | <span data-ttu-id="cccf6-121">REG \_ 二進位檔</span><span class="sxs-lookup"><span data-stu-id="cccf6-121">REG\_BINARY</span></span><br/> | <span data-ttu-id="cccf6-122">二進位陣列，描述辨識器設計來使用的語言或語言。</span><span class="sxs-lookup"><span data-stu-id="cccf6-122">Binary array describing the language or languages that a recognizer is designed to work with.</span></span><br/> <span data-ttu-id="cccf6-123">在 rectypes 中，[最大 \_ 語言] 定義會指定辨識器所支援的最大語言數目，而每個語言都會使用一個單字來儲存「可辨識的語言」專案。</span><span class="sxs-lookup"><span data-stu-id="cccf6-123">In rectypes.h, the MAX\_LANGUAGES define specifies the maximum number of languages supported by a recognizer, and each language takes a WORD to store in the "Recognized Languages" item.</span></span> <span data-ttu-id="cccf6-124">REG \_ 二進位登錄專案的大小應該是 \_ \* sizeof (WORD) 的最大語言。</span><span class="sxs-lookup"><span data-stu-id="cccf6-124">The size of the REG\_BINARY registry entry should be MAX\_LANGUAGES \* sizeof(WORD).</span></span><br/> |



 

 

 




