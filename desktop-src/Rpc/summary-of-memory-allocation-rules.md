---
title: 記憶體配置規則的摘要
description: 下表摘要說明有關記憶體配置的重要規則。
ms.assetid: 0c1f8398-75e6-45ec-a9f9-9dcdbe21c24d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f9403bb5057b2004d966c0634bc101a3282fe92
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104092967"
---
# <a name="summary-of-memory-allocation-rules"></a>記憶體配置規則的摘要

下表摘要說明有關記憶體配置的重要規則。



| MIDL 元素                                                                                                                                           | Description                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最上層 \[ [ref](/windows/desktop/Midl/ref) \] 指標                                                                                                                | 必須為非 null 指標。                                                                                                                                            |
| 函數傳回值                                                                                                                                  | 一律會為指標傳回值配置新的記憶體。                                                                                                             |
| \[[unique](/windows/desktop/Midl/unique)、 [out](/windows/desktop/Midl/out-idl) \] 或 \[ [ptr](/windows/desktop/Midl/ptr)、out \] 指標                                                                   | MIDL 不允許。                                                                                                                                                  |
| 非最上層的 \[ [unique](/windows/desktop/Midl/unique)、 [in](/windows/desktop/Midl/in)、 [out](/windows/desktop/Midl/out-idl) \] 或 \[ [ptr](/windows/desktop/Midl/ptr)、in、out \] 指標，從 null 變更為非 null | 用戶端 stub 會在傳回時于用戶端上配置新的記憶體。                                                                                                                 |
| \[ [](/windows/desktop/Midl/unique)從非 null 變更為 null 的非最上層 unique、 [in](/windows/desktop/Midl/in)、 [out](/windows/desktop/Midl/out-idl) \] 指標                                 | 用戶端上的記憶體是孤立的，用戶端應用程式負責釋放記憶體和防止流失。                                                              |
| 非最上層 \[ [ptr](/windows/desktop/Midl/ptr)、 [in](/windows/desktop/Midl/in)、 [out](/windows/desktop/Midl/out-idl) \] 指標，從非 null 變更為 null                                       | 用戶端上的記憶體如果沒有別名，就會是孤立的。在此情況下，用戶端應用程式會負責釋放和避免記憶體流失。                             |
| \[[參考](/windows/desktop/Midl/ref) \]指標                                                                                                                           | 用戶端應用層通常會配置。                                                                                                                           |
| 非 null \[ [in](/windows/desktop/Midl/in)、 [out](/windows/desktop/Midl/out-idl) \] 指標                                                                                                | 存根嘗試寫入至用戶端上現有的儲存體。 如果 **\[ 字串 \]** 和大小增加到超過用戶端所配置的大小，它會在傳回時造成 GP 錯誤。 |



 

下表摘要說明在記憶體管理上的金鑰識別碼L 和 ACF 屬性的影響。



| MIDL 功能                                                                   | 用戶端問題                                                                                                                                  | 伺服器問題                                                                                                                 |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| \[[配置](/windows/desktop/Midl/allocate) (單一 \_ 節點) \] 、 \[ 配置 (所有 \_ 節點) \]         | 判斷是否對記憶體函數進行一或多個呼叫。                                                                         | 與用戶端相同，不同之處在于私人記憶體通常可以用於配置 (單一 \_ 節點) \[ in \] 和 \[ in、out \] 資料。               |
| \[配置 (免費) \] 或 \[ 配置 (不 \_ 免費) \]                                 |  (無;會影響伺服器. )                                                                                                                         | 判斷是否要在每次遠端程序呼叫之後釋放伺服器上的記憶體。                                            |
| 陣列屬性 \[ [ \_ 的最大值](/windows/desktop/Midl/max-is)為 \] ，且 \[ [大小 \_ 為](/windows/desktop/Midl/size-is)\] |  (無;會影響伺服器. )                                                                                                                         | 判斷要配置的記憶體大小。                                                                                    |
| \[[位元組 \_ 計數](/windows/desktop/Midl/byte-count)\]                                            | 用戶端必須配置緩衝區;用戶端存根未配置或釋放。                                                                           | ACF 參數屬性會決定伺服器上配置的緩衝區大小。                                                        |
| \[[啟用 \_ 配置](/windows/desktop/Midl/enable-allocate)\]                                  | 通常是無。 不過，用戶端可能會使用不同的記憶體管理環境。                                                     | 伺服器使用不同的記憶體管理環境。 [**RpcSmAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmallocate) 應該用於配置。 |
| \[[in](/windows/desktop/Midl/in) \]屬性                                                    | 負責配置資料記憶體的用戶端應用程式。                                                                                 | 依存根配置於伺服器上。                                                                                                 |
| \[[out](/windows/desktop/Midl/out-idl) \]屬性                                             | 依存根配置於用戶端。                                                                                                                  | \[[out](/windows/desktop/Midl/out-idl) \]-只有指標必須是 \[ [ref](/windows/desktop/Midl/ref) \] 指標; 在伺服器上由存根配置。                       |
| \[[參考](/windows/desktop/Midl/ref) \]屬性                                                 | 指標所參考的記憶體必須由用戶端應用程式配置。                                                                          | 由存根管理的最上層和第一個層級參考指標。                                                                |
| \[[唯一](/windows/desktop/Midl/unique) \]屬性                                           | 非 null 至 null 可能會導致孤立的記憶體;null 為非 null 會導致用戶端 stub 呼叫 [midl \_ 使用者 \_ 配置](/windows/desktop/Midl/midl-user-allocate-1)。 |  (會影響用戶端 ) 。                                                                                                             |
| \[[ptr](/windows/desktop/Midl/ptr) \]屬性                                                 |  (請參閱 \[ [唯一](/windows/desktop/Midl/unique) \] 的 ) 。                                                                                                              |  (請參閱 \[ [唯一](/windows/desktop/Midl/unique) \] 的 ) 。                                                                                             |



 

 

 