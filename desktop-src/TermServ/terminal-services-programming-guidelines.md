---
title: 遠端桌面服務程式設計指導方針
description: 本主題提供在遠端桌面服務環境中開發應用程式的指導方針。
ms.assetid: e0cd52c5-40d7-4a48-9d10-fdbcea46a5a0
ms.tgt_platform: multiple
keywords:
- 遠端桌面服務遠端桌面服務，程式設計指導方針
- 程式設計指導方針遠端桌面服務
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e767740a2f279c90ce4f0eb37c49919749465ad1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106968705"
---
# <a name="remote-desktop-services-programming-guidelines"></a>遠端桌面服務程式設計指導方針

大部分現有的32位或64位 Windows 架構應用程式會在先前稱為終端機服務) 環境的遠端桌面服務 (中以相同的方式執行。 不過，有些應用程式在遠端桌面服務環境中正常運作並正常運作，而有些則沒有。 下列主題提供在遠端桌面服務環境中開發應用程式的指導方針。

## <a name="in-this-section"></a>本節內容

<dl> <dt>

[多使用者指導方針](multiple-user-guidelines.md)
</dt> <dd>

在遠端桌面服務環境中為多個使用者開發應用程式的指導方針。

</dd> <dt>

[效能指導方針](performance-guidelines.md)
</dt> <dd>

開發在遠端桌面服務環境中順利執行之應用程式的指導方針。

</dd> <dt>

[一般程式設計指導方針](general-programming-guidelines.md)
</dt> <dd>

在遠端桌面服務環境中開發應用程式的指導方針。

</dd> </dl>

其中許多指導方針都是良好的程式設計實務，可受益于在任何 Windows 環境中執行的應用程式。 不過，某些建議的優化（例如限制圖形效果）是優化，只有在您的應用程式在遠端桌面服務下執行時，才會想要優化。 如需說明如何偵測遠端桌面服務環境的程式碼範例，請參閱偵測 [遠端桌面服務環境](detecting-the-terminal-services-environment.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>


</dt> <dt>

[終端機服務現在遠端桌面服務](terminal-services-is-now-remote-desktop-services.md)
</dt> <dt>

[系統管理範本檔案格式](/previous-versions/windows/desktop/Policy/administrative-template-file-format)
</dt> <dt>

[登錄機碼安全性與存取權限](/windows/desktop/SysInfo/registry-key-security-and-access-rights)
</dt> <dt>

[登錄 hive](/windows/desktop/SysInfo/registry-hives)
</dt> <dt>

[安全性描述項](/windows/desktop/SecAuthZ/security-descriptors)
</dt> <dt>

[標準存取權限](/windows/desktop/SecAuthZ/standard-access-rights)
</dt> <dt>

[存取控制模型](/windows/desktop/SecAuthZ/access-control-model)
</dt> </dl>

 

 