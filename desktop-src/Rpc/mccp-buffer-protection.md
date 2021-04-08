---
title: MCCP 緩衝區保護
description: 從 Windows Vista 開始，RPC 封送處理引擎會採取進一步的步驟來嘗試防止用戶端緩衝區溢位，因為傳回的資料。 這項功能稱為「迷你計算一致性保護」 (MCCP) 。
ms.assetid: 37fe743b-c64e-469d-b8f4-abab9f05c813
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a70d04de57974bd9665d659129590d72513eb83e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682982"
---
# <a name="mccp-buffer-protection"></a>MCCP 緩衝區保護

從 Windows Vista 開始，RPC 封送處理引擎會採取進一步的步驟來嘗試防止用戶端緩衝區溢位，因為傳回的資料。 這項功能稱為「迷你計算一致性保護」 (MCCP) 。

當用戶端將現有緩衝區的指標傳遞至 \[ [**out**](/windows/desktop/Midl/out-idl) \] 或 \[ [**in**](/windows/desktop/Midl/in)、**out** \] 參數時，會將該參數傳回的資料複製到現有的緩衝區。 如果傳回的資料大於傳遞的緩衝區，當 RPC 將傳回的資料複製到太小的緩衝區時，就會發生緩衝區溢位。 請參閱 [最上層和內嵌指標](top-level-and-embedded-pointers.md)。

使用 MCCP 時，RPC 會嘗試偵測此狀況，並在偵測到時拒絕呼叫。 針對具有相互關聯值的緩衝區，例如 \[ [**大小 \_ 為**](/windows/desktop/Midl/size-is) \] ，如果傳回的資料不符合指定的緩衝區大小，則會拒絕呼叫並 \_ 引發 RPC X \_ 錯誤的 \_ 存根 \_ 資料例外狀況。 針對可變大小字串，如果現有的字串大小 (長度，直到 **null** 結束字元) 不足以容納傳回的字串時，會拒絕呼叫，則會拒絕呼叫。 在所有情況下，RPC 都無法偵測緩衝區溢位，因此，建議開發人員繼續對緩衝區溢位採取正常的預防措施。

如果用戶端未傳遞 out 參數的現有緩衝區 \[ [](/windows/desktop/Midl/out-idl) \] ，而是將可取值的指標傳遞至 **Null**，RPC 將會遵循一般規則來代表用戶端配置新的緩衝區。 這個緩衝區將配置足夠的空間來保存傳回的資料。

第二種保護是針對相互關聯的參數，RPC 會強制在相互關聯計數變數非 **null** 時傳遞非 **null** 的緩衝區。

``` syntax
HRESULT PassString( [in] DWORD Length, [in, unique, string, size_is( Length )]LPWSTR MyString );
```

如果 *MyString* 為 **Null**，RPC 將會拒絕呼叫，除非 *Length* 設定為0。 請注意，當 *MyString* 為非 **Null** 時，rpc 將允許 *長度* 為0，而 rpc 會將 *MyString* 視為0長度的緩衝區配置。

 

 