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
# <a name="structured-storage-fundamentals"></a>結構化儲存基礎

結構化儲存體提供對等的完整檔案系統，可透過下表所列的元素來儲存物件。



| 元素                                                                  | 描述                                                                                                                                                                                                                                                                                                                                                    |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [結構化儲存介面](structured-storage-interfaces.md)       | [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)、 [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream)、 [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes)和 [**IRootStorage**](/windows/desktop/api/Objidl/nn-objidl-irootstorage)介面，以及一組相關的介面-[**IPersistStorage**](/windows/win32/api/objidl/nn-objidl-ipersiststorage)、 [**IPersist**](/windows/win32/api/objidl/nn-objidl-ipersist)、 [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile)和 [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream)。 |
| [結構化儲存體 API 函數](structured-storage-api-functions.md) | 協助程式的 Api，可加速結構化儲存區的執行，以及第二組的複合檔案 Api;這是結構化儲存介面的 COM 執行。 COM 也提供一組支援的結構和列舉值，可用來組織介面方法和 Api 的參數。                              |
| [結構化儲存體存取模式](structured-storage-access-modes.md)   | 一組用來控管複合檔案存取權的存取模式。                                                                                                                                                                                                                                                                                                 |



 

 

 