---
title: 結構化儲存基礎
description: 結構化儲存體提供對等的完整檔案系統來儲存物件。
ms.assetid: 7e2d6211-2ea0-4cad-9388-c789b12446ab
keywords:
- 結構化儲存體 Strctd Stg.，基本概念
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d93b74afd620edca5b6beaa43bde6fff43d7263
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842416"
---
# <a name="structured-storage-fundamentals"></a><span data-ttu-id="5c138-104">結構化儲存基礎</span><span class="sxs-lookup"><span data-stu-id="5c138-104">Structured Storage Fundamentals</span></span>

<span data-ttu-id="5c138-105">結構化儲存體提供對等的完整檔案系統，可透過下表所列的元素來儲存物件。</span><span class="sxs-lookup"><span data-stu-id="5c138-105">Structured Storage provides the equivalent of a complete file system for storing objects through the elements listed in the following table.</span></span>



| <span data-ttu-id="5c138-106">元素</span><span class="sxs-lookup"><span data-stu-id="5c138-106">Element</span></span>                                                                  | <span data-ttu-id="5c138-107">描述</span><span class="sxs-lookup"><span data-stu-id="5c138-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                                    |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5c138-108">結構化儲存介面</span><span class="sxs-lookup"><span data-stu-id="5c138-108">Structured Storage Interfaces</span></span>](structured-storage-interfaces.md)       | <span data-ttu-id="5c138-109">[**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)、 [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream)、 [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes)和 [**IRootStorage**](/windows/desktop/api/Objidl/nn-objidl-irootstorage)介面，以及一組相關的介面-[**IPersistStorage**](/windows/win32/api/objidl/nn-objidl-ipersiststorage)、 [**IPersist**](/windows/win32/api/objidl/nn-objidl-ipersist)、 [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile)和 [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream)。</span><span class="sxs-lookup"><span data-stu-id="5c138-109">The [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage), [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream), [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes), and [**IRootStorage**](/windows/desktop/api/Objidl/nn-objidl-irootstorage) interfaces, along with a set of related interfaces —[**IPersistStorage**](/windows/win32/api/objidl/nn-objidl-ipersiststorage), [**IPersist**](/windows/win32/api/objidl/nn-objidl-ipersist), [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile), and [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream).</span></span> |
| [<span data-ttu-id="5c138-110">結構化儲存體 API 函數</span><span class="sxs-lookup"><span data-stu-id="5c138-110">Structured Storage API Functions</span></span>](structured-storage-api-functions.md) | <span data-ttu-id="5c138-111">協助程式的 Api，可加速結構化儲存區的執行，以及第二組的複合檔案 Api;這是結構化儲存介面的 COM 執行。</span><span class="sxs-lookup"><span data-stu-id="5c138-111">Helper APIs that facilitate an implementation of structured storage, as well as a second set of APIs for compound files; that is the COM implementation of the structured storage interfaces.</span></span> <span data-ttu-id="5c138-112">COM 也提供一組支援的結構和列舉值，可用來組織介面方法和 Api 的參數。</span><span class="sxs-lookup"><span data-stu-id="5c138-112">COM also provides a set of supporting structures and enumeration values used to organize parameters for interface methods and APIs.</span></span>                              |
| [<span data-ttu-id="5c138-113">結構化儲存體存取模式</span><span class="sxs-lookup"><span data-stu-id="5c138-113">Structured Storage Access Modes</span></span>](structured-storage-access-modes.md)   | <span data-ttu-id="5c138-114">一組用來控管複合檔案存取權的存取模式。</span><span class="sxs-lookup"><span data-stu-id="5c138-114">A set of access modes for regulating access to compound files.</span></span>                                                                                                                                                                                                                                                                                                 |



 

 

 