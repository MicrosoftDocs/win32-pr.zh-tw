---
description: 通告動作是一種最上層的動作，稱為用以安裝或移除已公告的元件。
ms.assetid: d9c843e4-fcd9-4d47-9ca9-ffa83ed80574
title: 通告動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0985990d69863f250cfd6f589deb43a59f9c66e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103692804"
---
# <a name="advertise-action"></a>通告動作

通告動作是一種最上層的動作，稱為用以安裝或移除已公告的元件。

## <a name="sequence-restrictions"></a>順序限制

沒有任何順序限制。

## <a name="actiondata-messages"></a>ActionData 訊息

沒有任何 ActionData 訊息。

## <a name="remarks"></a>備註

[*廣告*](a-gly.md) 指的是，安裝程式能夠提供應用程式的載入和啟動介面，而不需要實際安裝應用程式。 在使用者或應用程式啟動已公告的介面之前，安裝程式不會安裝必要的元件。 這個概念稱為 [*隨選安裝*](i-gly.md)。

未從動作資料表序列內呼叫公告動作，Windows Installer 會在使用 '/j ' 命令列參數呼叫命令列可執行檔 Msiexec.exe，或呼叫 [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) 時，將 *szCommandLine* 參數設定為 action = 通告時執行此動作。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[AdvtExecuteSequence 資料表](advtexecutesequence-table.md)
</dt> </dl>

 

 



