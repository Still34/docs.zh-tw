---
title: 如何：設定應用程式的 ToolStrip 產生器
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Renderer property [Windows Forms]
- ToolStripProfessionalRenderer class [Windows Forms]
- ToolStrip control [Windows Forms]
- MenuStrip control [Windows Forms]
- toolbars [Windows Forms], customizing
ms.assetid: 46acef3e-9844-4ae8-9a2e-3006fe99cadf
ms.openlocfilehash: b86724bda83c701ad5c5872ae8d97bb490158e76
ms.sourcegitcommit: 5bbfe34a9a14e4ccb22367e57b57585c208cf757
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/17/2018
ms.locfileid: "45698230"
---
# <a name="how-to-set-the-toolstrip-renderer-for-an-application"></a>如何：設定應用程式的 ToolStrip 產生器
您可以針對個別的 <xref:System.Windows.Forms.ToolStrip> 控制項，或是應用程式中的所有 <xref:System.Windows.Forms.ToolStrip> 控制項自訂外觀。  
  
## <a name="example"></a>範例  
 下列程式碼範例示範如何選擇性地將自訂轉譯器套用至 <xref:System.Windows.Forms.ToolStrip> 控制項和 <xref:System.Windows.Forms.MenuStrip> 控制項。  
  
 若要使用此程式碼範例，請編譯並執行應用程式，然後從 <xref:System.Windows.Forms.ComboBox> 控制項選取自訂轉譯的範圍。 按一下 [套用] 以設定轉譯器。  
  
 若要查看自訂功能表項目轉譯，請選取<xref:System.Windows.Forms.MenuStrip>選項<xref:System.Windows.Forms.ComboBox>控制項中按一下 **套用**，然後開啟**檔案**功能表項目。  
  
 [!code-csharp[System.Windows.Forms.ToolStrip.Misc#1](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.Misc/CS/Program.cs#1)]
 [!code-vb[System.Windows.Forms.ToolStrip.Misc#1](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.Misc/VB/Program.vb#1)]  
[!code-csharp[System.Windows.Forms.ToolStrip.Misc#70](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.Misc/CS/Program.cs#70)]
[!code-vb[System.Windows.Forms.ToolStrip.Misc#70](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.Misc/VB/Program.vb#70)]  
  
 設定 <xref:System.Windows.Forms.ToolStripManager.Renderer%2A?displayProperty=nameWithType> 屬性，以將自訂轉譯器套用至應用程式中的所有 <xref:System.Windows.Forms.ToolStrip> 控制項。  
  
 設定 <xref:System.Windows.Forms.ToolStrip.Renderer%2A?displayProperty=nameWithType> 屬性，以將自訂轉譯器套用至個別的 <xref:System.Windows.Forms.ToolStrip> 控制項。  
  
## <a name="compiling-the-code"></a>編譯程式碼  
 這個範例需要：  
  
-   System.Design、System.Drawing 和 System.Windows.Forms 組件的參考。  
  
 建置此範例從命令列 visual Basic 或 Visual C# 的相關資訊，請參閱[從命令列建置](~/docs/visual-basic/reference/command-line-compiler/building-from-the-command-line.md)或是[命令列使用 csc.exe 建置](~/docs/csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md)。 您也可以將程式碼貼入新的專案，以建置此範例的 Visual Studio。  另請參閱[如何：使用 Visual Studio 編譯及執行完整的 Windows Forms 程式碼範例](https://msdn.microsoft.com/library/Bb129228\(v=vs.110\))。  
  
## <a name="see-also"></a>另請參閱  
 <xref:System.Windows.Forms.ToolStripManager>  
 <xref:System.Windows.Forms.MenuStrip>  
 <xref:System.Windows.Forms.ToolStrip>  
 <xref:System.Windows.Forms.ToolStripProfessionalRenderer>  
 [ToolStrip 控制項](../../../../docs/framework/winforms/controls/toolstrip-control-windows-forms.md)
