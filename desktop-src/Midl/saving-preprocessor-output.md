---
title: 正在儲存預處理器輸出
description: 查看預處理器輸出可能是有效的疑難排解方法，例如，當發生不正確 IDL、C 或 C 預處理器語法時，或 MIDL 命令列上的偽 D 值導致 MIDL 報告難懂錯誤時。
ms.assetid: 79c53f0c-c179-4731-a2c3-a1022d378e7b
keywords:
- MIDL 編譯器 MIDL，儲存預處理器輸出
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49ca1e07658fb2da525999e396b7c3da27add385
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372305"
---
# <a name="saving-preprocessor-output"></a>正在儲存預處理器輸出

查看預處理器輸出可能是有效的疑難排解方法，例如，當發生不正確 IDL、C 或 C 預處理器語法時，或 MIDL 命令列上的偽 D 值導致 MIDL 報告難懂錯誤時。 開發人員也可能想要檢查預處理器輸出，以判斷編譯器輸入資料流程中有哪些檔案和定義，例如必須解決類型重新定義衝突的困難案例。 或者，某些開發人員可能會想要在預處理器上使用 [**/cpp \_ opt**](-cpp-opt.md)來強制執行私用參數，或可能想要查看切換開關的運作方式。

從 MIDL 編譯執行取得前置處理過的檔案，最簡單且最不內斂的方式是使用 [**-savePP**](-savepp.md) 參數。 **-SavePP** 參數只會防止 MIDL 刪除預處理器傳回 MIDL 的暫存檔案。 請考慮下列事項：

**midl-savePP-Id： \\ nt \\ public \\ SDK \\ inc.-DNTENV = 1-Oicf-env win32 stub .idl**

這個指示詞會編譯 Stub，但仍會保留所有預處理器檔案。

> [!Note]  
> 如果有) 以及每個匯入的檔案，MIDL 會為 IDL 和 ACF 檔案 (產生個別的預處理器執行。

 

針對 DCOM 編譯，通常會產生數個預處理器檔案，即使 MIDL 以虛擬連續輸入資料流程的方式處理也是一樣。 在一般的 Windows 程式設計環境中，可以在臨時目錄中找到暫存檔案，以作為檔案名，例如 \* MID。 如果保留預處理器輸出，最好先監看 Temp 目錄中的最新檔案，以識別哪些檔案與預處理器執行相關聯。

在簡單的情況下，例如編譯的 IDL 檔案不會直接或間接匯入其他檔案，或是在檢查最上層檔案時，可以直接叫用預處理器。 直接執行 C/c + + 預處理器可能會顯示由 MIDL 遮罩或混淆的錯誤。 例如，下列兩個預處理器命令列可以用於前面加上引號的 MIDL 行：

**cl/E/nologo-Id： \\ nt \\ public \\ SDK \\ inc.-DNTENV = 1 存根 .idl > stub. pp**

**cl/E/P-Id： \\ nt \\ public \\ SDK \\ inc.-DNTENV = 1 stub**

在這兩個範例的第一個範例中， **/e** [**/nologo**](-nologo.md) 是 MIDL 叫用預處理器時新增的參數。 預處理器輸出會傳送到 stdout (畫面) ，因此需要重新導向至檔案以進行檢查。 在這些範例的第二個範例中， **/p** 會指示預處理器將輸出重新導向至檔案 \* 。在此情況下，會在目前的目錄中建立檔案。

[**/Cpp \_ opt**](-cpp-opt.md)參數也可以用來取得前置處理過的檔案，但對於先前提及的方法而言很困難且較差。 下列範例也會產生如先前範例所示的存根檔案。 下列範例中的引號是必要的：

**Midl-Oicf-win32-cpp \_ opt "/E/p-Id： \\ nt \\ public \\ sdk \\ inc.-DNTENV = 1" stub**

 

 




