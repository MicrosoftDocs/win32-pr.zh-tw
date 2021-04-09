---
title: 多執行緒用戶端和內容控制碼
description: 當您的多執行緒用戶端有多個執行緒使用相同的內容控制碼實例時，預設會在伺服器上序列化內容控制碼實例的存取。
ms.assetid: 192be467-b1e0-422b-878a-738cb7d72b5b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67c621d75d8cc48ca1f71719066f455e0efce39f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023789"
---
# <a name="multithreaded-clients-and-context-handles"></a>多執行緒用戶端和內容控制碼

當您的多執行緒用戶端有多個執行緒使用相同的內容控制碼實例時，預設會在伺服器上序列化內容控制碼實例的存取。 如此一來，伺服器管理員就不需要針對來自相同用戶端的另一個執行緒進行防護，也就是在分派呼叫時，變更內容或正在執行的內容。 不過，在某些情況下，序列化可能會影響效能。

請考慮下列各項：兩個用戶端執行緒叫用不會變更內容狀態的遠端程序呼叫 (例如，呼叫只會從它) 取得一些值。 這類呼叫不需要序列化。

在這種情況下，Windows XP 會提供混合模式的序列化模型，其中每個方法都可以宣告為具有內容控制碼的獨佔或共用存取。 如需詳細資料，請參閱 [內容 \_ 控制碼 \_ 序列化](/windows/desktop/Midl/context-handle-serialize) 和 [內容 \_ 控制碼 \_ noserialize](/windows/desktop/Midl/context-handle-noserialize) 。

在 Windows XP 之前的 Windows 版本中，允許平行存取內容控制碼的唯一方法，就是呼叫 [**RpcSsDontSerializeCoNtext**](/previous-versions/aa378473(v=vs.80)) 函式，以允許在單一內容控制碼上分派多個呼叫。 呼叫 **RpcSsDontSerializeCoNtext** 函數並不會完全停用序列化;當發生內容執行時，只有在所有未完成的用戶端要求都已完成時，才會執行內容執行常式。 對 **RpcScDontSerializeCoNtext** 的呼叫會影響整個進程，且不會還原。 不建議在 Windows XP 和更新版本中使用 **RpcScDontSerializeCoNtext** ;它會讓伺服器程式碼在處理完全非序列化環境固有的競爭條件時變得非常複雜。

 

 