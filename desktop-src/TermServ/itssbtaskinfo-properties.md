---
title: ITsSbTaskInfo 屬性
description: ITsSbTaskInfo 介面會公開下列屬性。
ms.assetid: 402B8502-DE17-440B-867D-45922582C30E
ms.tgt_platform: multiple
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c0e4c8fefc2e443778b2ce177e61a314a3e0ef9
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "103678388"
---
# <a name="itssbtaskinfo-properties"></a>ITsSbTaskInfo 屬性

[**ITsSbTaskInfo**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskinfo)介面會公開下列屬性。

## <a name="in-this-section"></a>本節內容

<dl> <dt>

[**CoNtext 屬性**](itssbtaskinfo-context.md)
</dt> <dd>

捕獲與工作相關聯的內容位元組。

</dd> <dt>

[**期限屬性**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtaskinfo-get_deadline)
</dt> <dd>

抓取必須起始工作的時間。 這是用來排列修補程式的優先順序。 系統會先起始最早期限的修補程式。

</dd> <dt>

[**EndTime 屬性**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtaskinfo-get_endtime)
</dt> <dd>

抓取工作代理程式可以啟動工作的最晚時間。

</dd> <dt>

[**[識別項] 屬性**](itssbtaskinfo-identifier.md)
</dt> <dd>

抓取由工作代理程式當做唯一識別碼使用的 GUID。

</dd> <dt>

[**標籤屬性**](itssbtaskinfo-label.md)
</dt> <dd>

抓取描述工作用途的標籤。

</dd> <dt>

[**外掛程式屬性**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtaskinfo-get_plugin)
</dt> <dd>

抓取工作代理程式的顯示名稱。

</dd> <dt>

[**StartTime 屬性**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtaskinfo-get_starttime)
</dt> <dd>

抓取工作代理程式可以啟動工作的最早時間。

</dd> <dt>

[**Status 屬性**](itssbtaskinfo-status.md)
</dt> <dd>

抓取 [**RDV 工作 \_ \_ 狀態**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status) 列舉值，這個值表示工作的狀態。

</dd> <dt>

[**TargetId 屬性**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtaskinfo-get_targetid)
</dt> <dd>

抓取目標識別碼。

</dd> </dl>

 

 




