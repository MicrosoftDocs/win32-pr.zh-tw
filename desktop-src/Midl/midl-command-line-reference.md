---
title: MIDL Command-Line 參考
description: 本節包含 Microsoft RPC MIDL 編譯器可辨識的每個命令列參數和切換選項的參考資訊。
ms.assetid: a0e5efb0-a704-4dc5-bd7e-6c98466a2874
keywords:
- Microsoft 介面定義語言 MIDL，參考
- 命令列參考 MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1569e29daf8a2976379576a5f1671f5117e7990c
ms.sourcegitcommit: 9cf1ed65dfbea1ba118b63d0656f30c3685d8520
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106969828"
---
# <a name="midl-command-line-reference"></a>MIDL Command-Line 參考

本節包含 Microsoft RPC MIDL 編譯器可辨識的每個命令列參數和切換選項的參考資訊。 交換器專案會依字母順序排列。 [一般 MIDL 命令列語法](general-midl-command-line-syntax.md) 描述一般命令列語法。

<dl>

[一般 MIDL 命令列語法](general-midl-command-line-syntax.md)  
[回應檔命令](the-response-file-command.md)  
[**/acf**](-acf.md)  
[**/align**](-align.md)  
[**/amd64**](-amd64.md)  
[**/app \_ 設定**](-app-config.md)  
[/backward \_ 相容性](-backward-compat.md)  
[**/c \_ ext**](-c-ext.md)  
[**/caux**](-caux.md)  
[**/char**](-char.md)  
[**/client**](-client.md)  
[**/confirm**](-confirm.md)  
[**/cpp \_ cmd**](-cpp-cmd.md)  
[**/cpp \_ opt**](-cpp-opt.md)  
[**/cstruct_out**](-cstruct-out.md) 
[ **/cstub**](-cstub.md)  
[**/D**](-d.md)  
[**/dlldata**](-dlldata.md)  
[**/env**](-env.md)  
[**/error**](-error.md)  
[**/error**](-error.md)  
[**/h**](-h.md)  
[**/header**](-header.md)  
[**/help (/？ )**](-help-.md)  
[**/ia64**](-ia64.md)  
[**/I**](-i.md)  
[**/iid**](-iid.md)  
[**/import**](-import.md)  
[**/lcid**](-lcid.md)  
[**/mktyplib203**](-mktyplib203.md)  
[**/ms \_ ext**](-ms-ext.md)  
[**/ms 聯 \_ 集**](-ms-union.md)  
[**/msc \_ ver**](-msc-ver.md)  
[**/new**](-new.md)  
[**/newtlb**](-newtlb.md)  
[**/no \_ cpp、/nocpp**](-no-cpp-nocpp.md)  
[**/no \_ 預設 \_ epv**](-no-default-epv.md)  
[**/no \_ def \_ idir**](-no-def-idir.md)  
[**/no \_ 格式 \_ 選擇**](-no-format-opt.md)  
[**/no \_ 健全**](-no-robust.md)  
[**/no \_ 警告**](-no-warn.md)  
[**/nologo**](-nologo.md)  
[**/notlb**](-notlb.md)  
[**/o**](-o.md)  
[**/Oi**](-oi.md)  
[**/old**](-old.md)  
[**/oldtlb**](-oldtlb.md)  
[**/oldnames**](-oldnames.md)  
[**/Os**](-os.md)  
[**/osf**](-osf.md)  
[**/out**](-out.md)  
[**/pack**](-pack.md)  
[**/prefix**](-prefix.md)  
[**/protocol**](-protocol.md)  
[**/proxy**](-proxy.md)  
[**/robust**](-robust.md)  
[**/rpcss**](-rpcss.md)  
[**/sal**](-sal.md)  
[**/sal \_ 本機**](-sal-local.md)  
[**/saux**](-saux.md)  
[**/savePP**](-savepp.md)  
[**/sstub**](-sstub.md)  
[**/syntax \_ 檢查**](-syntax-check.md)  
[**/<system>**](-system-.md)  
[**/target**](-target.md)  
[**/tlb**](-tlb.md)  
[**U**](-u.md)  
[**/use \_ epv**](-use-epv.md)  
[**/version \_ 戳記**](-version-stamp.md)  
[**/W**](-w.md)  
[**/warn**](-warn.md)  
[**/win32**](-win32.md)  
[**/win64**](-win64.md)  
[**/WX**](-wx.md)  
[**/Zp**](-zp.md)  
[**/Zs**](-zs.md)  
</dl>

MIDL 編譯器可以針對不同的平臺和系統版本產生程式碼。 請參閱 [**/target**](-target.md) 參數，以深入瞭解建議的參數，以及如何產生針對特定版本優化的程式碼。

請注意，負號 ( – ) 可能會取代所有 MIDL 命令列參數中以斜線 (/) 開頭的斜線 (/) 。 下列範例將示範叫用 MIDL 編譯器時的等價。

## <a name="examples"></a>範例

**midl/acf my \_ acf. acf** *filename * * * .idl**

**midl-acf my \_ acf. acf** *filename * * * .idl**

 

 




