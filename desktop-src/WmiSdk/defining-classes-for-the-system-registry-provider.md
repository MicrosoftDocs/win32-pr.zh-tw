---
description: 使用系統登錄提供者的管理應用程式可以定義類別，其屬性代表特定金鑰的登錄資料，然後將類別儲存在 WMI 存放庫中。
ms.assetid: e8707a3d-a393-4be0-9e86-297f0af15d99
ms.tgt_platform: multiple
title: 定義 System Registry 提供者的類別
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ebce4867559398722182b7b77ae02bc31c070b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944798"
---
# <a name="defining-classes-for-the-system-registry-provider"></a><span data-ttu-id="0e7bb-103">定義 System Registry 提供者的類別</span><span class="sxs-lookup"><span data-stu-id="0e7bb-103">Defining Classes for the System Registry Provider</span></span>

<span data-ttu-id="0e7bb-104">使用系統登錄提供者的管理應用程式可以定義類別，其屬性代表特定金鑰的登錄資料，然後將類別儲存在 WMI 存放庫中。</span><span class="sxs-lookup"><span data-stu-id="0e7bb-104">A management application using the System Registry provider can define classes with properties that represent registry data for particular keys and then stores the classes in the WMI repository.</span></span> <span data-ttu-id="0e7bb-105">針對系統登錄定義類別的大部分程式，與定義任何其他類別的程式相同。</span><span class="sxs-lookup"><span data-stu-id="0e7bb-105">Most of the processes for defining a class for the system registry is identical to defining any other class.</span></span> <span data-ttu-id="0e7bb-106">不過，系統登錄提供者會要求您使用特定的資料類型和限定詞。</span><span class="sxs-lookup"><span data-stu-id="0e7bb-106">However, the System Registry provider requires that you use specific data types and qualifiers.</span></span>

<span data-ttu-id="0e7bb-107">下列程式說明如何定義 System Registry 提供者的類別。</span><span class="sxs-lookup"><span data-stu-id="0e7bb-107">The following procedure describes how to define a class for the System Registry provider.</span></span>

<span data-ttu-id="0e7bb-108">**若要定義 System Registry 提供者的類別**</span><span class="sxs-lookup"><span data-stu-id="0e7bb-108">**To define a class for the System Registry provider**</span></span>

1.  <span data-ttu-id="0e7bb-109">建立類別的方式，就像任何其他類別一樣。</span><span class="sxs-lookup"><span data-stu-id="0e7bb-109">Create the class as you would any other class.</span></span>

    <span data-ttu-id="0e7bb-110">如需詳細資訊，請參閱 [建立類別](creating-a-class.md)。</span><span class="sxs-lookup"><span data-stu-id="0e7bb-110">For more information, see [Creating a Class](creating-a-class.md).</span></span>

2.  <span data-ttu-id="0e7bb-111">將適當的登錄資料類型對應至適當的 WMI 類型。</span><span class="sxs-lookup"><span data-stu-id="0e7bb-111">Map the appropriate registry data types to the appropriate WMI types.</span></span>

    <span data-ttu-id="0e7bb-112">System Registry provider 將登錄資料類型對應至特定的 WMI 資料類型。</span><span class="sxs-lookup"><span data-stu-id="0e7bb-112">The System Registry provider maps the registry data types to specific WMI data types.</span></span> <span data-ttu-id="0e7bb-113">如需詳細資訊，請參閱將登錄 [資料類型對應至 WMI 資料類型](mapping-a-registry-data-type-to-a-wmi-data-type.md)。</span><span class="sxs-lookup"><span data-stu-id="0e7bb-113">For more information, see [Mapping a Registry Data Type to a WMI Data Type](mapping-a-registry-data-type-to-a-wmi-data-type.md).</span></span>

3.  <span data-ttu-id="0e7bb-114">使用必要的限定詞來定義登錄提供者的位置，以及適當登錄機碼的位置。</span><span class="sxs-lookup"><span data-stu-id="0e7bb-114">Use the required qualifiers to define the location of the Registry provider and the location of the appropriate registry key.</span></span>

    <span data-ttu-id="0e7bb-115">系統登錄提供者會使用三個限定詞來定義各種類別、提供者和登錄專案的位置。</span><span class="sxs-lookup"><span data-stu-id="0e7bb-115">The System Registry provider uses three qualifiers to define the location of various classes, providers, and registry entries.</span></span> <span data-ttu-id="0e7bb-116">如需詳細資訊，請參閱 [使用限定詞定義登錄類別](defining-a-registry-class-with-qualifiers.md)。</span><span class="sxs-lookup"><span data-stu-id="0e7bb-116">For more information, see [Defining a Registry Class With Qualifiers](defining-a-registry-class-with-qualifiers.md).</span></span>

 

 



