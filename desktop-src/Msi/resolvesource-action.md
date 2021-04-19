---
description: ResolveSource 動作會決定來源的位置，如果尚未解析來源，則會設定 SourceDir 屬性。
ms.assetid: 6d6205a0-a870-4df2-922b-befea7e28a1a
title: ResolveSource 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 713598cd4daa90764cde2155e43b61e151432d31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988368"
---
# <a name="resolvesource-action"></a>ResolveSource 動作

ResolveSource 動作會決定來源的位置，如果尚未解析來源，則會設定 [**SourceDir**](sourcedir.md) 屬性。

## <a name="sequence-restrictions"></a>順序限制

ResolveSource 動作必須晚于 [CostInitialize 動作](costinitialize-action.md)。

## <a name="actiondata-messages"></a>ActionData 訊息

沒有任何 ActionData 訊息。

## <a name="remarks"></a>備註

在任何運算式中使用 [**SourceDir**](sourcedir.md) 屬性之前，必須先呼叫 ResolveSource 動作。 您也必須先呼叫它，才能嘗試使用 [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya)抓取 **SourceDir** 屬性的值。 當來源無法使用時，不應執行 ResolveSource 動作，因為它可能會在卸載應用程式時執行。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[來源復原](source-resiliency.md)
</dt> </dl>

 

 



