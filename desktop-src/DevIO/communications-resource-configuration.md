---
description: COMMCONFIG 結構會定義通訊資源的設定，也就是序列或其他方式。
ms.assetid: 05094b98-4694-42dd-883c-b3c90735b3bc
title: 通訊資源設定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c6d19bb8478590c85c9f0c1d60ce91cbd1b802a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110701"
---
# <a name="communications-resource-configuration"></a>通訊資源設定

[**COMMCONFIG**](/windows/desktop/api/Winbase/ns-winbase-commconfig)結構會定義通訊資源的設定，也就是序列或其他方式。 結構的格式會根據 (提供者子類型) 的通訊資源類型而有所不同。 前幾個結構成員通用於所有通訊資源;針對特定提供者子類型定義其他成員。 特定服務提供者也可以擴充 **COMMCONFIG** 結構。

應用程式可以使用 [**GetCommConfig**](/windows/desktop/api/Winbase/nf-winbase-getcommconfig) 和 [**SetCommConfig**](/windows/desktop/api/Winbase/nf-winbase-setcommconfig) 函數來取得和設定通訊資源的設定。 開啟時，會使用其提供者子類型的預設設定來初始化通訊資源。 若要取得並設定提供者子類型的預設設定，請使用 [**GetDefaultCommConfig**](/windows/desktop/api/Winbase/nf-winbase-getdefaultcommconfiga) 和 [**SetDefaultCommConfig**](/windows/desktop/api/Winbase/nf-winbase-setdefaultcommconfiga) 函數。

若要提示使用者輸入設定資訊，請使用 [**CommConfigDialog**](/windows/desktop/api/Winbase/nf-winbase-commconfigdialoga) 函數。 此函式會顯示服務提供者定義的對話方塊，並根據使用者輸入填入 [**COMMCONFIG**](/windows/desktop/api/Winbase/ns-winbase-commconfig) 結構。

 

 



