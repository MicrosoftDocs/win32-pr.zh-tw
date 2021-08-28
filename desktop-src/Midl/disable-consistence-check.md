---
title: disable_consistency_check 屬性
description: 指示 RPC 不要強制執行相互關聯一致性檢查。
ms.assetid: 33ba331d-56e5-4965-a844-7780ea81623d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc88112ac80462daa6c1babdd29799ccf05e33bb4edb52de1ffbbbb00e71352b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117807223"
---
# <a name="disable_consistency_check-attribute"></a>停用 \_ 一致性 \_ 檢查屬性

指示 RPC 不要強制執行相互關聯一致性檢查。

``` syntax
interface interface-name
{
  return-type function-name(
        [[attribute-list,] disable_consistency_check] param-type param-name
}
```

針對相互關聯的參數，RPC 會強制在相互關聯計數變數為非 null 時傳遞非 null 的緩衝區。

## <a name="example"></a>範例

``` syntax
HRESULT PassString( [in] DWORD Length, [in, unique, string, 
    size_is( Length )]LPWSTR MyString );
```

如果 *MyString* 為 **Null**，RPC 將會拒絕呼叫，除非 Length 設定為0。 請注意，當 *MyString* 為非 Null 時，rpc 將允許 *長度* 為0，而 rpc 會將 *MyString* 視為0長度的緩衝區配置。

## <a name="remarks"></a>備註

若要停用這種檢查，IDL 可以 \[ \_ \_ \] 在參數、typedef 或指標類型上包含停用一致性檢查屬性。 這會將 RPC 導向，使其不會強制執行參數或指標所指向之緩衝區的緩衝區指標和相互關聯變數之間的一致性。

若要停用整個 MIDL 編譯 (的一致性檢查，並在所有情況下停用強制檢查) ，可以使用 MIDL 命令列參數 [/backward \_ 相容性 maybenull \_ sizeis](-backward-compat.md) 。 這需要 MIDL 編譯的目標至少為 "target NT60"。

 

 




