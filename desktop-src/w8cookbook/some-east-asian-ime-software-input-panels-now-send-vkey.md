---
title: 某些東亞 IME 軟體輸入面板現在會傳送 vKey
description: 某些東亞 IME 軟體輸入面板現在會傳送 vKey
ms.assetid: 5E3BE112-D962-4C11-B31E-229584191FAE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c444091e4498582cccc4378dfa2f17216cbf810
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840896"
---
# <a name="some-east-asian-ime-software-input-panels-now-send-vkey"></a>某些東亞 IME 軟體輸入面板現在會傳送 vKey

## <a name="platforms"></a>平台

<dl> 用戶端-Windows 8。1  
伺服器-Windows Server 2012 R2  
</dl>

## <a name="description"></a>Description

在 Windows 8 中，如果選取其中一個東亞 Ime，則按下軟體輸入面板鍵不會傳送 vKeys。

在 Windows 8.1 中，會針對下列設定傳送 vKeys：



| 語言            | IME                                 | Windows 市集 | 桌面 |
|---------------------|-------------------------------------|---------------|---------|
| 簡體中文  | Microsoft 拼音，Microsoft Wubi    | 是           | 是     |
| 繁體中文 | Microsoft Changlie，Microsoft 快速 | 是           | 是     |
| 繁體中文 | Microsoft 注音                  | 否            | 否      |
| 韓文              | [Microsoft IME]                       | 是           | 否      |
| 日文            | [Microsoft IME]                       | 否            | 否      |



 

## <a name="manifestations"></a>表現

如果使用者選擇不傳送 vKeys 的輸入法，vKey 觸發的函式將無法運作。

## <a name="solution"></a>解決方法

未使用上述其中一個 IME 設定的應用程式，必須設計成讓使用者可以完成所需的工作，而不需要使用需要 vKeys 的函式。

如果使用者選擇執行傳送 vKeys 的輸入法，但應用程式是在不預期的情況下設計的，則必須變更應用程式，以辨識正在執行的 Windows 版本，並據以回應。

 

 




