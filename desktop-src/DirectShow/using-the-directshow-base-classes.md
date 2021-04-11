---
description: 使用 DirectShow 基類
ms.assetid: 7eab0e55-1566-4b4c-b37c-32c5a1f37363
title: 使用 DirectShow 基類
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 870c910505d6df42d0b9a6094470bf803b83d6b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193527"
---
# <a name="using-the-directshow-base-classes"></a>使用 DirectShow 基類

若要在 DirectShow 中使用基底類別，您必須建立並連結基類庫。

Base 類別庫是以 Microsoft Windows 軟體開發套件 (SDK)  () 中的 SDK 範例形式提供 <https://go.microsoft.com/fwlink/p/?linkid=62332> 。 確切的位置取決於您已安裝的 SDK 版本，但相對路徑為：

*(SDK 範例根)* \\DirectShow \\ BaseClasses

標頭：資料流程。h

程式庫：此範例會建立程式庫的零售版和偵錯工具版本：

-   零售版： Strmbase .lib
-   Debug version： Strmbasd .lib。

如需設定組建環境的詳細資訊，請參閱 [設定組建環境](setting-up-the-build-environment.md)。

## <a name="preprocessor-symbols"></a>前置處理器符號

當您包含標頭檔串流 .h 時，下列預處理器符號具有特殊意義：

-   效能：已保留。 請勿使用這個預處理器符號。
-   VFWROBUST：啟用零售的指標驗證。 如需詳細資訊，請參閱 [指標驗證宏](pointer-validation-macros.md)。 在 debug 組建中，您不需要定義 VFWROBUST。

> [!Note]  
> 在 Windows Vista 和更新版本中，指標驗證宏是空的。

 

 

 



