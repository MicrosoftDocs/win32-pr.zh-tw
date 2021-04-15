---
title: 作業外掛程式進入點
description: 作業外掛程式進入點
ms.assetid: 9a3ddc2b-9fde-4915-b0e8-0a5e79e73c00
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0834363c7447bc50269da09d361e630d9bc0615a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463160"
---
# <a name="operations-plug-in-entry-points"></a>作業外掛程式進入點

作業外掛程式需要根據其想要支援的功能來執行特定的進入點。

外掛程式必須註冊 Windows 遠端管理 (WinRM) 服務，其中包含外掛程式 DLL 進入點的名稱。 所有作業都有預先定義的 DLL 進入點，如果支援該作業，就必須公開這些進入點。

下表概述 WinRM 外掛程式 API 中的操作外掛程式進入點。



| 函式                                                                                 | 描述                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WSMAN \_ 外掛程式 \_ 命令**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_command)                                   | 定義外掛程式的命令回呼。<br/> 所有支援 shell 功能的 WinRM 外掛程式都必須執行此回呼。<br/> 此方法的 DLL 進入點名稱必須是 [**WSManPluginCommand**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_command)。<br/> |
| [**WSMAN \_ 外掛程式 \_ 連接**](/windows/desktop/api/WsMan/nc-wsman-wsman_plugin_connect)                                   | 定義外掛程式的連接回呼。<br/> 此方法的 DLL 進入點名稱必須是 [**WSManPluginConnect**](/windows/desktop/api/WsMan/nc-wsman-wsman_plugin_connect)。<br/>                                                                                                |
| [**WSMAN \_ 外掛程式 \_ 接收**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_receive)                                   | 定義外掛程式的接收回呼。<br/> 所有支援 shell 功能的 WinRM 外掛程式都必須執行此回呼。<br/> 此方法的 DLL 進入點名稱必須是 [**WSManPluginReceive**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_receive)。<br/> |
| [**WSMAN \_ 外掛程式 \_ 釋放 \_ 命令 \_ 內容**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_release_command_context) | 定義外掛程式的發行命令回呼。<br/> DLL 進入點名稱必須是 [**WSManPluginReleaseCommandCoNtext**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_release_command_context)。<br/>                                                                        |
| [**WSMAN \_ 外掛程式 \_ 版本 \_ SHELL \_ 內容**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_release_shell_context)     | 定義外掛程式的 release shell 回呼。<br/> DLL 進入點名稱必須是 [**WSManPluginReleaseCommandCoNtext**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_release_command_context)。<br/>                                                                          |
| [**WSMAN \_ 外掛程式 \_ 傳送**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_send)                                         | 定義外掛程式的傳送回呼。<br/> 所有支援 shell 功能的 WinRM 外掛程式都必須執行此回呼。<br/> 此方法的 DLL 進入點名稱必須是 [**WSManPluginSend**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_send)。<br/>          |
| [**WSMAN \_ 外掛程式 \_ SHELL**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_shell)                                       | 定義外掛程式的 shell 回呼。<br/> 所有支援 shell 功能的 WinRM 外掛程式都必須執行此回呼。<br/> 此方法的 DLL 進入點名稱必須是 [**WSManPluginShell**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_shell)。<br/>       |
| [**WSMAN \_ 外掛程式 \_ 關機**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_shutdown)                                 | 定義外掛程式的關機回呼。<br/> 所有 WinRM 外掛程式都必須執行此回呼函數。<br/> 此方法的 DLL 進入點名稱必須是 [**WSManPluginShutdown**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_shutdown)。<br/>                      |
| [**WSMAN \_ 外掛程式 \_ 信號**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_signal)                                     | 定義外掛程式的信號回呼。<br/> 所有支援 shell 功能的 WinRM 外掛程式都必須執行此回呼。<br/> 此方法的 DLL 進入點名稱必須是 [**WSManPluginSignal**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_signal)。<br/>    |
| [**WSMAN \_ 外掛程式 \_ 啟動**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_startup)                                   | 定義外掛程式的啟動回呼。<br/> 所有 WinRM 外掛程式都必須執行此回呼函數。<br/> 此方法的 DLL 進入點名稱必須是 [**WSManPluginStartup**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_startup)。<br/>                         |



 

 

