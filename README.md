##DIAGRAM_SPEC_START##
META	agent	SOP Agent
META	product	Test
LANE	PC	Product Control
NODE	N1	PC	start	Begin Process
NODE	N2	PC	process	Validate Data
NODE	N3	PC	end	Complete Process
EDGE	N1	N2
EDGE	N2	N3
##DIAGRAM_SPEC_END##
