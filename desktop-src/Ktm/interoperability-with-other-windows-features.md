---
description: 分散式交易協調器 (DTC) 可在一或多個系統上控制多個資源管理員的分散式交易或交易。 KTM 和 DTC 密切合作以達成此目的。
ms.assetid: 468379e2-c5f6-479f-9d5d-42afb395ec9b
title: 與其他 Windows 功能的互通性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa3aeac3d920b408a9a18c32eab83cf747525e82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987661"
---
# <a name="interoperability-with-other-windows-features"></a><span data-ttu-id="5d5f5-104">與其他 Windows 功能的互通性</span><span class="sxs-lookup"><span data-stu-id="5d5f5-104">Interoperability With Other Windows Features</span></span>

<span data-ttu-id="5d5f5-105">[分散式交易協調器](/previous-versions/windows/desktop/ms684146(v=vs.85)) (DTC) 可在一或多個系統上控制多個資源管理員的 *分散式交易* 或交易。</span><span class="sxs-lookup"><span data-stu-id="5d5f5-105">The [Distributed Transaction Coordinator](/previous-versions/windows/desktop/ms684146(v=vs.85)) (DTC) enables *distributed transactions*, or transactions that are under the control of multiple resource managers on one or more systems.</span></span> <span data-ttu-id="5d5f5-106">KTM 和 DTC 密切合作以達成此目的。</span><span class="sxs-lookup"><span data-stu-id="5d5f5-106">KTM and DTC work closely together to accomplish this.</span></span>

<span data-ttu-id="5d5f5-107">COM + 會公開交易式程式設計的宣告式模型。</span><span class="sxs-lookup"><span data-stu-id="5d5f5-107">COM+ exposes a declarative model for transactional programming.</span></span> <span data-ttu-id="5d5f5-108">換句話說，程式設計人員會宣告物件可利用交易的範圍，而 COM + 執行時間代表物件管理交易。</span><span class="sxs-lookup"><span data-stu-id="5d5f5-108">In other words, the programmer declares the extent to which an object can take advantage of transactions, and the COM+ runtime manages the transactions on the object's behalf.</span></span> <span data-ttu-id="5d5f5-109">例如，您只能將物件宣告為參與交易（如果已經存在的話），若要要求交易 (則會建立交易（如果它不 () 存在的話），而不論是否已存在) 或非交易式都會建立一個交易。</span><span class="sxs-lookup"><span data-stu-id="5d5f5-109">For example, an object can be declared to participate in a transaction only if one already exists, to require a transaction (one is created if it does not already exist), to require a new transaction (one is created regardless of whether one already exists), or is not transactional.</span></span> <span data-ttu-id="5d5f5-110">這些以宣告方式管理的交易會自動用於在交易內容中執行的 COM + 物件所建立的資料庫連接上。</span><span class="sxs-lookup"><span data-stu-id="5d5f5-110">These declaratively-managed transactions are automatically used on database connections created by COM+ objects that are executing in the context of a transaction.</span></span>

 

 
